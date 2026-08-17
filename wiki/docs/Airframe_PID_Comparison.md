---
geometry: margin=0.5in, landscape=true
mainfont: DejaVu Sans
fontsize: 8pt
---

# Airframe PID Parameter Comparison

All 12 airframes from `originaldefaults.h` converted to unified float `.af` format. 
Values are in FC-native units (radians, volts, fractions — not degrees, volts×10, or percent).

## Rate PID Gains

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
RollRateKp & 0.16 & 0.095 & 0.1 & 0.16 & 0.095 & 0.16 & 0.04 & 0.095 & 0.1 & 0.06 & 0.2 & 0.04 \\
RollRateKd & 0.006 & 0.004 & 0.0045 & 0.006 & 0.004 & 0.006 & 0 & 0.004 & 0.0045 & 0 & 0.004 & 0 \\
\bottomrule
\end{longtable}
## Angle PID Gains

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
RollAngleQKp & 7 & 5.75 & 7 & 7 & 5.75 & 7 & 2 & 5.75 & 7 & 3 & 0.75 & 2 \\
RollAngleQKi & 0.1 & 0.15 & 0.25 & 0.2 & 0.15 & 0.1 & 0.1 & 0.15 & 0.25 & 0.15 & 0.1 & 0.1 \\
RollAngleQIntLimit & 0.005236 & 0.002618 & 0.002618 & 0.00733 & 0.002618 & 0.005236 & 0.002618 & 0.002618 & 0.002618 & 0.002618 & 0.002618 & 0.002618 \\
\bottomrule
\end{longtable}
## Pitch Axis

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
PitchRateKp & 0.16 & 0.095 & 0.1 & 0.16 & 0.095 & 0.16 & 0.04 & 0.095 & 0.1 & 0.1 & 0.2 & 0.04 \\
PitchRateKd & 0.006 & 0.004 & 0.0045 & 0.006 & 0.004 & 0.006 & 0 & 0.004 & 0.0045 & 0 & 0.004 & 0 \\
PitchAngleQKp & 7 & 5.75 & 7 & 7 & 5.75 & 7 & 2 & 5.75 & 7 & 7.5 & 0.75 & 2 \\
PitchAngleQKi & 0.1 & 0.15 & 0.25 & 0.1 & 0.15 & 0.1 & 0.1 & 0.15 & 0.25 & 0.4 & 0.1 & 0.1 \\
PitchAngleQIntLimit & 0.005236 & 0.002618 & 0.002618 & 0.00733 & 0.002618 & 0.005236 & 0.002618 & 0.002618 & 0.002618 & 0.003927 & 0.002618 & 0.002618 \\
\bottomrule
\end{longtable}
## Yaw Axis

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
YawRateKp & 0.2 & 0.125 & 0.1 & 0.2 & 0.125 & 0.2 & 0.05 & 0.125 & 0.1 & 0.05 & 0.05 & 0.05 \\
YawRateKd & 0.000125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 & 0.000125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 \\
YawAngleQKp & 2.25 & 3 & 3 & 3 & 3 & 2.25 & 3 & 3 & 3 & 3 & 3 & 3 \\
YawAngleQKi & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 \\
YawAngleQIntLimit & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 \\
\bottomrule
\end{longtable}
## Navigation Gains

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
NavPosKp & 0.33 & 0.2475 & 0.2475 & 0.2475 & 0.2475 & 0.33 & 0.33 & 0.2475 & 0.33 & 0.33 & 0.33 & 0.33 \\
NavPosKi & 0.008 & 0.012 & 0.012 & 0.012 & 0.012 & 0.008 & 0.008 & 0.012 & 0.008 & 0.008 & 0.008 & 0.008 \\
NavVelKp & 0.6 & 0.6 & 0.3 & 0.6 & 0.6 & 0.6 & 0.6 & 0.3 & 0.6 & 0.6 & 0.6 & 0.6 \\
\bottomrule
\end{longtable}
## Altitude Gains

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
AltPosKp & 0.5124 & 0.5124 & 0.5124 & 0.1464 & 0.4575 & 0.915 & 0.2928 & 0.4392 & 0.5124 & 0.2928 & 0.2928 & 0.2928 \\
AltPosKi & 0.0046 & 0.0046 & 0.0046 & 0.00092 & 0.00184 & 0.0138 & 0.00552 & 0.00276 & 0.0046 & 0.00552 & 0.00552 & 0.00552 \\
\bottomrule
\end{longtable}
## Cruise & Limits

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450-1165 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
EstCruiseThr & 0.59 & 0.3 & 0.54 & 0.31 & 0.3 & 0.54 & 0.2 & 0.5 & 0.55 & 0.2 & 0.2 & 0.2 \\
MaxRollAngle & 1.0472 & 1.0472 & 0.523599 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
MaxPitchAngle & 1.0472 & 1.0472 & 0.523599 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 0.523599 & 1.0472 & 1.0472 \\
NavMaxAngle & 0.261799 & 0.349066 & 0.436332 & 0.349066 & 0.349066 & 0.261799 & 0.349066 & 0.261799 & 0.349066 & 0.698132 & 0.349066 & 0.349066 \\
BatteryCapacity & 22 & 22 & 22 & 22 & 22 & 22 & 22 & 50 & 22 & 22 & 22 & 22 \\
LowVoltThres & 3.4 & 9.6 & 9.6 & 13.6 & 13.8 & 3 & 10.2 & 10 & 10.2 & 10.2 & 10.2 & 10.2 \\
RCChannels & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 \\
MaxRollRate & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
MaxPitchRate & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
\bottomrule
\end{longtable}

