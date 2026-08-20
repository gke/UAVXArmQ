---
geometry: margin=0.5in, landscape=true
mainfont: DejaVu Sans
fontsize: 8pt
---

# Airframe Parameter Comparison

All FC parameters in unified-float format (radians, volts, fractions).
**Bold** values are dramatic outliers relative to the airframe set median.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
RollRateKp & 0.1 & 0.15 & 0.24 & 0.2 & 0.3 & 0.095 & 0.16 & 0.095 & 0.16 \\
AltPosKi & 0.0046 & 0.003 & 0.004 & 0.003 & 0.004 & 0.00276 & 0.00092 & 0.00184 & \textbf{0.0138} \\
RollAngleQKp & 7 & 7 & \textbf{8} & 7 & \textbf{8} & \textbf{5.75} & 7 & \textbf{5.75} & 7 \\
RollAngleQIntLimit & 0.002618 & 0.003 & \textbf{0.005} & 0.003 & \textbf{0.005} & 0.002618 & \textbf{0.00733} & 0.002618 & \textbf{0.005236} \\
PitchRateKp & 0.1 & 0.18 & 0.28 & 0.22 & 0.32 & 0.095 & 0.16 & 0.095 & 0.16 \\
AltPosKp & 0.5124 & 0.45 & 0.5 & 0.55 & 0.65 & 0.4392 & \textbf{0.1464} & 0.4575 & \textbf{0.915} \\
PitchAngleQKp & 7 & 7 & \textbf{8} & 7 & \textbf{8} & \textbf{5.75} & 7 & \textbf{5.75} & 7 \\
PitchAngleQIntLimit & 0.002618 & 0.003 & \textbf{0.005} & 0.003 & \textbf{0.005} & 0.002618 & \textbf{0.00733} & 0.002618 & \textbf{0.005236} \\
YawRateKp & 0.1 & 0.18 & 0.26 & 0.15 & 0.25 & 0.125 & 0.2 & 0.125 & 0.2 \\
RollRateKd & 0.0045 & 0.012 & 0.008 & 0.006 & 0.004 & 0.004 & 0.006 & 0.004 & 0.006 \\
BbLogType & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
RxThrottleCh & 0 & 0 & 0 & 0 & 0 & \textbf{2} & 0 & 0 & 0 \\
LowVoltThres & 9.6 & 9.6 & 9.6 & 9.6 & 9.6 & \textbf{10} & \textbf{13.6} & \textbf{13.8} & \textbf{3} \\
RollCamKp & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 \\
EstCruiseThr & 0.54 & 0.55 & 0.55 & 0.6 & 0.6 & 0.5 & \textbf{0.31} & \textbf{0.3} & 0.54 \\
StickHysteresis & 0.02 & 0.02 & 0.02 & 0.02 & 0.02 & 0.02 & \textbf{0.04} & \textbf{0.03} & 0.02 \\
FwClimbThrottle & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
PercentIdleThr & 0.05 & 0.05 & 0.05 & 0.05 & 0.05 & \textbf{0.1} & \textbf{0.1} & 0.05 & \textbf{0.1} \\
RollAngleQKi & 0.25 & 0.25 & 0.2 & 0.25 & 0.2 & 0.15 & 0.2 & 0.15 & 0.1 \\
PitchAngleQKi & 0.25 & 0.25 & 0.2 & 0.25 & 0.2 & 0.15 & 0.1 & 0.15 & 0.1 \\
PitchCamKp & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 \\
ServoLpfHz & 25 & 25 & 25 & 25 & 25 & 25 & \textbf{10} & 25 & 25 \\
PitchRateKd & 0.0045 & 0.012 & 0.008 & 0.008 & 0.005 & 0.004 & 0.006 & 0.004 & 0.006 \\
NavVelKp & 0.3 & 0.25 & 0.35 & 0.3 & 0.4 & 0.3 & \textbf{0.6} & \textbf{0.6} & \textbf{0.6} \\
Horizon & 0.3 & 0.3 & 0.5 & 0.3 & 0.5 & 0.4 & 0.4 & 0.4 & 0.3 \\
MadgwickKpMag & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & \textbf{0} & 0.5 & \textbf{0.4} & 0.5 \\
NavRthAlt & 10 & 10 & 10 & 10 & 10 & \textbf{5} & 10 & 10 & 10 \\
NavMagVar & \textbf{0.205949} & 0.223402 & 0.223402 & 0.223402 & 0.223402 & \textbf{0.059341} & 0.226893 & \textbf{0.204204} & 0.226893 \\
RcChannels & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 \\
RxRollCh & \textbf{1} & 0 & 0 & 0 & 0 & 0 & \textbf{1} & \textbf{1} & \textbf{1} \\
MadgwickKpAcc & 0.2 & 0.2 & \textbf{0.25} & 0.2 & \textbf{0.25} & \textbf{0.05} & 0.2 & \textbf{0.18} & 0.2 \\
RollCamTrim & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.01} & 0 & 0 \\
NavPosIntLimit & 3 & 5 & 6 & 5 & 6 & 3 & 5 & 5 & 8 \\
RxPitchCh & 2 & 0 & 0 & 0 & 0 & 1 & 2 & 2 & 2 \\
RxYawCh & 3 & \textbf{0} & \textbf{0} & \textbf{0} & \textbf{0} & 3 & 3 & 3 & 3 \\
MaxDescentRateDmpS & 10 & 10 & 10 & 10 & 10 & \textbf{9} & \textbf{18} & \textbf{30} & \textbf{12} \\
DescentDelayS & 15 & 15 & 15 & 15 & 15 & \textbf{10} & \textbf{10} & \textbf{10} & 15 \\
GyroLpfSel & 2 & 2 & \textbf{1} & 2 & \textbf{1} & 2 & 2 & 2 & 2 \\
NavCrossTrackKp & 0.04 & 0.04 & \textbf{0.05} & 0.04 & \textbf{0.05} & 0.04 & 0.04 & 0.04 & 0.04 \\
RxGearCh & 4 & \textbf{0} & \textbf{0} & \textbf{0} & \textbf{0} & 5 & 5 & 5 & 5 \\
RxAux1Ch & 5 & 0 & 0 & 0 & 0 & 6 & 8 & 11 & 8 \\
ServoSense & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{9} \\
AccConfSd & 0.06 & 0.06 & 0.06 & 0.06 & 0.06 & \textbf{0.02} & 0.06 & \textbf{0.04} & 0.06 \\
BatteryCapacity & 22 & \textbf{2200} & \textbf{2200} & \textbf{2200} & \textbf{2200} & 50 & 22 & 22 & 22 \\
RxAux2Ch & 6 & 0 & 0 & 0 & 0 & 4 & 6 & 6 & 6 \\
RxAux3Ch & 10 & 0 & 0 & 0 & 0 & 8 & 7 & 7 & 7 \\
NavPosKp & 0.2475 & \textbf{0.22} & \textbf{0.28} & 0.25 & \textbf{0.3} & 0.2475 & 0.2475 & 0.2475 & \textbf{0.33} \\
AltLpf & 10 & 10 & 10 & 10 & 10 & 10 & \textbf{20} & 10 & \textbf{20} \\
Balance & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 \\
RxAux4Ch & 8 & 0 & 0 & 0 & 0 & 11 & 11 & 8 & 10 \\
NavPosKi & 0.012 & 0.012 & \textbf{0.015} & 0.012 & \textbf{0.015} & 0.012 & 0.012 & 0.012 & \textbf{0.008} \\
TiltThrottleFf & 0 & 0 & 0 & 0 & 0 & \textbf{0.07} & \textbf{0.25} & \textbf{0.1} & 0 \\
MaxYawRate & 2.0944 & 1.5708 & 3.14159 & 1.5708 & 3.14159 & 3.49066 & 7.67945 & 5.23599 & 7.67945 \\
FwRollPitchFf & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.25} \\
FwPitchThrottleFf & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.1} \\
FwMaxClimbAngle & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & \textbf{0.261799} \\
NavMaxAngle & 0.436332 & 0.436332 & 0.523599 & 0.436332 & 0.523599 & 0.261799 & 0.349066 & 0.349066 & 0.261799 \\
FwSpoilerDecayPercentPs & 0.01 & 0.01 & 0.01 & 0.01 & 0.01 & \textbf{0} & \textbf{0} & \textbf{0} & \textbf{0.015} \\
FwAileronDifferential & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.3} \\
KfAccUBiasVar & \textbf{3e-06} & 0 & 0 & 0 & 0 & \textbf{1e-05} & \textbf{5e-06} & 0 & 0 \\
MaxPitchAngle & 0.523599 & 0.523599 & 0.785398 & 0.523599 & 0.785398 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
QuatGain & - & 4 & 4 & 4 & 4 & - & - & - & - \\
MaxRollAngle & 0.523599 & 0.523599 & 0.785398 & 0.523599 & 0.785398 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
YawLpfHz & 50 & 50 & \textbf{60} & 50 & \textbf{60} & 50 & 50 & 50 & \textbf{30} \\
NavHeadingTurnout & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 & \textbf{0.698132} \\
AltHoldThrCompDecayPercentPs & 0.025 & 0.03 & 0.03 & 0.03 & 0.03 & \textbf{0} & \textbf{0} & \textbf{0.001} & \textbf{0} \\
FwBoardPitchAngle & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.087266} \\
MaxRollRate & 10.472 & \textbf{6.28319} & 10.472 & \textbf{6.28319} & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
MaxPitchRate & 10.472 & \textbf{3.14159} & \textbf{6.28319} & \textbf{3.14159} & \textbf{6.28319} & 10.472 & 10.472 & 10.472 & 10.472 \\
CurrentScale & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 \\
VoltScale & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 \\
FwAileronRudderMix & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{1} \\
FwAltSpoilerFf & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.5} \\
MaxCompassYawRate & 1.0472 & 0.523599 & 0.523599 & 0.523599 & 0.523599 & 1.0472 & 1.0472 & 1.0472 & 1.5708 \\
AccLpfSel & 4 & 4 & \textbf{3} & 4 & \textbf{3} & 4 & 4 & 4 & 4 \\
YawRateKd & 0.001125 & \textbf{0.008} & \textbf{0.005} & 0.002 & 0.002 & 0.001125 & 0.001125 & 0.001125 & 0.000125 \\
ThrottleGainRate & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
RxAux5Ch & 9 & \textbf{0} & \textbf{0} & \textbf{0} & \textbf{0} & 9 & 9 & 9 & 9 \\
RxAux6Ch & 7 & 0 & 0 & 0 & 0 & 10 & 10 & 10 & 11 \\
RxAux7Ch & 11 & 0 & 0 & 0 & 0 & 7 & 4 & 4 & 4 \\
YawAngleQKp & 3 & \textbf{6} & \textbf{8} & 4 & 5 & 3 & 3 & 3 & 2.25 \\
YawAngleQKi & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 \\
YawAngleQIntLimit & 0.008727 & \textbf{0.025} & \textbf{0.03} & \textbf{0.015} & \textbf{0.02} & 0.008727 & 0.008727 & 0.008727 & 0.008727 \\
AltPosIntLimit & 0.5 & \textbf{0.25} & \textbf{0.3} & \textbf{0.35} & \textbf{0.4} & 0.5 & 0.5 & 0.5 & 0.5 \\
MotorStopSel & 0 & 0 & 0 & 0 & 0 & \textbf{0.002618} & 0 & 0 & 0 \\
AltThrottleCompLimit & 0.2 & 0.25 & 0.28 & 0.22 & 0.24 & 0.06 & 0.12 & 0.05 & 0.02 \\
VrsRoc & 50 & -3 & -3 & -3 & -3 & 30 & 30 & 30 & 50 \\
AhRocWindowMps & \textbf{20} & 1 & 1 & 1 & 1 & 15 & \textbf{30} & 5 & 5 \\
NavProxAltM & 4 & 4 & 4 & 4 & 4 & \textbf{2} & \textbf{3} & \textbf{3} & \textbf{5} \\
NavProxRadiusM & 3 & 3 & 3 & 3 & 3 & \textbf{2} & \textbf{2} & \textbf{1} & \textbf{10} \\
KfBaroVar & \textbf{100} & 1 & 1 & 1 & 1 & 20 & 50 & 50 & 50 \\
KfAccUVar & 0.2 & \textbf{2} & \textbf{2} & \textbf{2} & \textbf{2} & 0.2 & 0.2 & 0.2 & 0.2 \\
FwStickScale & 4 & 0.4 & 0.5 & 0.4 & 0.5 & 4 & 2 & 4 & 4 \\
FwRollControlPitchLimit & 0.785398 & \textbf{45.8366} & \textbf{45.8366} & \textbf{45.8366} & \textbf{45.8366} & 0.785398 & 0.785398 & 0.785398 & 0.785398 \\
AhThrottleMovingTrigger & 0.2 & 0.2 & 0.15 & 0.2 & 0.15 & 0.1 & 0.11 & 0.2 & 0.3 \\
NavFenceRadiusM & 100 & 400 & 400 & 400 & 400 & 100 & 200 & 100 & 100 \\
DiveRecoverAlt & - & 0 & 0 & 0 & 0 & - & - & - & - \\
\bottomrule
\end{longtable}
## Notes

- Outlier detection: values > 3 MAD from the median are bolded.
- Unused/reserved parameters omitted.






