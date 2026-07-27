---
geometry: margin=0.5in, landscape=true
mainfont: DejaVu Sans
fontsize: 8pt
---

# Airframe PID Comparison — Selected Airframes

Airframes: **Ecks 220**, **Ecks 0800 Mod**, **Ecks 0800 Sport**, **Ecks 1kg Mod**, **Ecks 1kg Sport**, **Rok's Quad**, **Ken's 450**, **Ken's Alpha**, **Ken's LadyBug**.
Values in unified float format (radians for angles, volts, fractions).

## Rate PID Gains

Rate Kp controls roll responsiveness; higher values = more aggressive. Rate Kd provides damping to reduce overshoot.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
RollRateKp & 0.1 & 0.15 & 0.24 & 0.2 & 0.3 & 0.095 & 0.16 & 0.095 & 0.16 \\
RollRateKd & 0.0045 & 0.012 & 0.008 & 0.006 & 0.004 & 0.004 & 0.006 & 0.004 & 0.006 \\
\bottomrule
\end{longtable}
## Angle PID Gains

Angle Kp controls attitude stiffness (return-to-level force). Ki eliminates steady-state error in hover. Int Limit caps the integrator windup.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
RollAngleKp & 7 & 7 & 8 & 7 & 8 & 5.75 & 7 & 5.75 & 7 \\
RollAngleKi & 0.25 & 0.25 & 0.2 & 0.25 & 0.2 & 0.15 & 0.2 & 0.15 & 0.1 \\
RollAngleIntLimit & 0.002618 & 0.003 & 0.005 & 0.003 & 0.005 & 0.002618 & 0.00733 & 0.002618 & 0.005236 \\
\bottomrule
\end{longtable}
## Pitch Axis

Pitch rate and angle gains — symmetric to roll by convention on symmetric multirotors.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
PitchRateKp & 0.1 & 0.18 & 0.28 & 0.22 & 0.32 & 0.095 & 0.16 & 0.095 & 0.16 \\
PitchRateKd & 0.0045 & 0.012 & 0.008 & 0.008 & 0.005 & 0.004 & 0.006 & 0.004 & 0.006 \\
PitchAngleKp & 7 & 7 & 8 & 7 & 8 & 5.75 & 7 & 5.75 & 7 \\
PitchAngleKi & 0.25 & 0.25 & 0.2 & 0.25 & 0.2 & 0.15 & 0.1 & 0.15 & 0.1 \\
PitchAngleIntLimit & 0.002618 & 0.003 & 0.005 & 0.003 & 0.005 & 0.002618 & 0.00733 & 0.002618 & 0.005236 \\
\bottomrule
\end{longtable}
## Yaw Axis

Yaw rate and angle gains — typically lower Kd than roll/pitch. Yaw angle is a weak hold, often overridden by heading-hold in navigation.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
YawRateKp & 0.1 & 0.18 & 0.26 & 0.15 & 0.25 & 0.125 & 0.2 & 0.125 & 0.2 \\
YawRateKd & 0.001125 & 0.008 & 0.005 & 0.002 & 0.002 & 0.001125 & 0.001125 & 0.001125 & 0.000125 \\
YawAngleKp & 3 & 6 & 8 & 4 & 5 & 3 & 3 & 3 & 2.25 \\
YawAngleKi & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 \\
YawAngleIntLimit & 0.008727 & 0.025 & 0.03 & 0.015 & 0.02 & 0.008727 & 0.008727 & 0.008727 & 0.008727 \\
\bottomrule
\end{longtable}
## Navigation Gains

Pos Kp/Ki control position-hold stiffness. Vel Kp controls max correction velocity toward target.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
NavPosKp & 0.2475 & 0.22 & 0.28 & 0.25 & 0.3 & 0.2475 & 0.2475 & 0.2475 & 0.33 \\
NavPosKi & 0.012 & 0.012 & 0.015 & 0.012 & 0.015 & 0.012 & 0.012 & 0.012 & 0.008 \\
NavVelKp & 0.3 & 0.25 & 0.35 & 0.3 & 0.4 & 0.3 & 0.6 & 0.6 & 0.6 \\
\bottomrule
\end{longtable}
## Altitude Gains

Alt Pos Kp/Ki control altitude-hold response. These work on top of the cruise throttle feedforward.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
AltPosKp & 0.5124 & 0.45 & 0.5 & 0.55 & 0.65 & 0.4392 & 0.1464 & 0.4575 & 0.915 \\
AltPosKi & 0.0046 & 0.003 & 0.004 & 0.003 & 0.004 & 0.00276 & 0.00092 & 0.00184 & 0.0138 \\
\bottomrule
\end{longtable}
## Cruise & Limits

Cruise throttle is the hover feedforward baseline. Angle/rate limits cap max attitude and rotation speed. Battery capacity and low-voltage threshold set the FC's voltage monitoring.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm} >{\raggedleft\arraybackslash}p{1.5cm}}
\toprule
Param & Ecks 220 & Ecks 0800 Mod & Ecks 0800 Sport & Ecks 1kg Mod & Ecks 1kg Sport & Rok's Quad & Ken's 450 & Ken's Alpha & Ken's LadyBug \\
\midrule
\endhead
EstCruiseThr & 0.54 & 0.55 & 0.55 & 0.6 & 0.6 & 0.5 & 0.31 & 0.3 & 0.54 \\
MaxRollAngle & 0.523599 & 0.523599 & 0.785398 & 0.523599 & 0.785398 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
MaxPitchAngle & 0.523599 & 0.523599 & 0.785398 & 0.523599 & 0.785398 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
NavMaxAngle & 0.436332 & 0.436332 & 0.523599 & 0.436332 & 0.523599 & 0.261799 & 0.349066 & 0.349066 & 0.261799 \\
BatteryCapacity & 22 & 2200 & 2200 & 2200 & 2200 & 50 & 22 & 22 & 22 \\
LowVoltThres & 9.6 & 9.6 & 9.6 & 9.6 & 9.6 & 10 & 13.6 & 13.8 & 3 \\
RCChannels & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 \\
MaxRollRate & 10.472 & 6.28319 & 10.472 & 6.28319 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
MaxPitchRate & 10.472 & 3.14159 & 6.28319 & 3.14159 & 6.28319 & 10.472 & 10.472 & 10.472 & 10.472 \\
\bottomrule
\end{longtable}
## Notes

- All values in FC-native units (radians for angles, volts, fractions).
- Ecks 220 is the original default from originaldefaults.h.
- Ecks 0800/1kg variants are manually tuned `.af` files in the GCS airframes directory.

