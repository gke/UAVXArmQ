---
geometry: margin=0.5in, landscape=true
fontsize: 8pt
---
# UAVX Failsafe Operation #

Modern receivers have failsafe capability where the channel values go to a known state if the transmitter signal is lost. It is IMPORTANT to set the failsafe values to something sensible e.g. RTH and not pitch/roll/yaw inputs. UAVX will attempt to do what the receiver commands.

## Failsafe Detection Paths ##

There are two independent paths that trigger failsafe behaviour, both handled in `MapRC()`:

1. **SBus failsafe flag**: `sbusDecode()` sets `RCFailsafe` directly from the SBus frame's failsafe bit. `MapRC()` then loads the failsafe presets into `RCInp[]`.

2. **Timeout**: `GenerateFailsafePacket()` detects sustained loss of valid packets and loads the failsafe presets into `RCInp[]` while also setting `RCFailsafe`.

Both paths converge to the same behaviour.

## Failsafe Presets ##

When failsafe is triggered, channel values are set to:

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{6.75cm} >{\raggedleft\arraybackslash}p{6.75cm}}
\toprule
Channel & Value & Effect \\
\midrule
\endhead
NavQual (Ch6) & 1650 µs (~65\%) & Arm + AltHold enabled \\
NavMode (Ch5) & 2000 µs & RTH selected \\
Roll/Pitch/Yaw & 1500 µs & Neutral sticks \\
Throttle & 1050 µs & Idle \\
\bottomrule
\end{longtable}
## Altitude Hold and Angle Mode Override ##

At the end of the NavQual processing block in `MapRC()`, if `RCFailsafe` or `RCSignalLost` is set, the code forces:
- **Altitude hold enabled** — overrides any other AltHold state
- **Angle mode** — overrides Horizon/Rate mode selections

This ensures the aircraft holds altitude and levels attitude regardless of the switch positions that were active before signal loss.

## PassThru Override ##

If `F.PassThru` is active, it overrides all failsafe behaviour:
- No nav or altitude hold actions
- Pilot-in-command (PIC) mode
- Direct stick-to-servo passthrough (mainly used for fixed wing)
- `F.PassThru` takes precedence over `RCFailsafe` and `RCSignalLost`




