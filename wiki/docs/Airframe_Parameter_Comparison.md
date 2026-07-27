---
geometry: margin=0.5in, landscape=true
mainfont: DejaVu Sans
fontsize: 8pt
---

# Airframe Parameter Comparison

All FC parameters in unified-float format (radians, volts, fractions).
**Bold** values are dramatic outliers relative to the airframe set median.

\begin{longtable}{>{\raggedright\arraybackslash}p{3.0cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm} >{\raggedleft\arraybackslash}p{1.758cm}}
\toprule
Param & 150mm Brushed & DevEBox & Ecks 220mm & Ken's 450 & Ken's Alpha & Ken's LadyBug & Phoenix FW & Rok's Quad & S500-1137 & Sky Surfer & Spoileron & Wing 900mm \\
\midrule
\endhead
RollRateKp & 0.16 & 0.095 & 0.1 & 0.16 & 0.095 & 0.16 & 0.04 & 0.095 & 0.1 & 0.06 & 0.2 & 0.04 \\
AltPosKi & 0.0046 & 0.0046 & 0.0046 & \textbf{0.00092} & \textbf{0.00184} & \textbf{0.0138} & 0.00552 & 0.00276 & 0.0046 & 0.00552 & 0.00552 & 0.00552 \\
RollAngleKp & 7 & 5.75 & 7 & 7 & 5.75 & 7 & 2 & 5.75 & 7 & 3 & \textbf{0.75} & 2 \\
RollAngleIntLimit & \textbf{0.005236} & 0.002618 & 0.002618 & \textbf{0.00733} & 0.002618 & \textbf{0.005236} & 0.002618 & 0.002618 & 0.002618 & 0.002618 & 0.002618 & 0.002618 \\
PitchRateKp & 0.16 & 0.095 & 0.1 & 0.16 & 0.095 & 0.16 & 0.04 & 0.095 & 0.1 & 0.1 & \textbf{0.2} & 0.04 \\
AltPosKp & 0.5124 & 0.5124 & 0.5124 & 0.1464 & 0.4575 & \textbf{0.915} & 0.2928 & 0.4392 & 0.5124 & 0.2928 & 0.2928 & 0.2928 \\
PitchAngleKp & 7 & 5.75 & 7 & 7 & 5.75 & 7 & \textbf{2} & 5.75 & 7 & 7.5 & \textbf{0.75} & \textbf{2} \\
PitchAngleIntLimit & \textbf{0.005236} & 0.002618 & 0.002618 & \textbf{0.00733} & 0.002618 & \textbf{0.005236} & 0.002618 & 0.002618 & 0.002618 & \textbf{0.003927} & 0.002618 & 0.002618 \\
YawRateKp & 0.2 & 0.125 & 0.1 & 0.2 & 0.125 & 0.2 & 0.05 & 0.125 & 0.1 & 0.05 & 0.05 & 0.05 \\
RollRateKd & 0.006 & 0.004 & 0.0045 & 0.006 & 0.004 & 0.006 & \textbf{0} & 0.004 & 0.0045 & \textbf{0} & 0.004 & \textbf{0} \\
BbLogType & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
Config1Bits & - & - & - & - & - & - & - & - & 0 & 0 & - & - \\
RxThrottleCh & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{2} & 0 & 0 & 0 & 0 \\
LowVoltThres & \textbf{3.4} & 9.6 & 9.6 & \textbf{13.6} & \textbf{13.8} & \textbf{3} & 10.2 & 10 & 10.2 & 10.2 & 10.2 & 10.2 \\
RollCamKp & 1 & 1 & 1 & 1 & 1 & 1 & \textbf{0} & 1 & 1 & \textbf{0} & \textbf{0} & \textbf{0} \\
EstCruiseThr & 0.59 & 0.3 & 0.54 & 0.31 & 0.3 & 0.54 & 0.2 & 0.5 & 0.55 & 0.2 & 0.2 & 0.2 \\
StickHysteresis & 0.02 & \textbf{0.03} & 0.02 & \textbf{0.04} & \textbf{0.03} & 0.02 & 0.02 & 0.02 & 0.02 & 0.02 & 0.02 & 0.02 \\
FwClimbThrottle & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.7} & 0 & 0 & \textbf{0.55} & \textbf{0.7} & \textbf{0.7} \\
PercentIdleThr & \textbf{0.1} & 0.05 & 0.05 & \textbf{0.1} & 0.05 & \textbf{0.1} & 0.05 & \textbf{0.1} & \textbf{0.1} & 0.05 & 0.05 & 0.05 \\
RollAngleKi & 0.1 & 0.15 & 0.25 & 0.2 & 0.15 & 0.1 & 0.1 & 0.15 & 0.25 & 0.15 & 0.1 & 0.1 \\
PitchAngleKi & 0.1 & 0.15 & \textbf{0.25} & 0.1 & 0.15 & 0.1 & 0.1 & 0.15 & \textbf{0.25} & \textbf{0.4} & 0.1 & 0.1 \\
PitchCamKp & 1 & 1 & 1 & 1 & 1 & 1 & \textbf{0} & 1 & 1 & \textbf{0} & \textbf{0} & \textbf{0} \\
ServoLpfHz & 25 & 25 & 25 & \textbf{10} & 25 & 25 & 25 & 25 & 25 & 25 & 25 & 25 \\
PitchRateKd & 0.006 & 0.004 & 0.0045 & 0.006 & 0.004 & 0.006 & \textbf{0} & 0.004 & 0.0045 & \textbf{0} & 0.004 & \textbf{0} \\
NavVelKp & 0.6 & 0.6 & \textbf{0.3} & 0.6 & 0.6 & 0.6 & 0.6 & \textbf{0.3} & 0.6 & 0.6 & 0.6 & 0.6 \\
Horizon & 0.3 & 0.4 & 0.3 & 0.4 & 0.4 & 0.3 & 0.01 & 0.4 & 0.3 & 0.01 & 0.01 & 0.01 \\
MadgwickKpMag & 0.5 & \textbf{0.4} & 0.5 & 0.5 & \textbf{0.4} & 0.5 & 0.5 & \textbf{0} & 0.5 & 0.5 & 0.5 & 0.5 \\
NavRthAlt & 10 & 10 & 10 & 10 & 10 & 10 & \textbf{30} & \textbf{5} & 10 & \textbf{30} & \textbf{30} & \textbf{30} \\
NavMagVar & 0.204204 & 0.204204 & \textbf{0.205949} & \textbf{0.226893} & 0.204204 & \textbf{0.226893} & 0.204204 & \textbf{0.059341} & 0.204204 & 0.204204 & 0.204204 & 0.204204 \\
RcChannels & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 & 7 \\
RxRollCh & 1 & 1 & 1 & 1 & 1 & 1 & 1 & \textbf{0} & 1 & 1 & 1 & 1 \\
MadgwickKpAcc & 0.2 & \textbf{0.18} & 0.2 & 0.2 & \textbf{0.18} & 0.2 & 0.2 & \textbf{0.05} & 0.2 & 0.2 & 0.2 & 0.2 \\
RollCamTrim & 0 & 0 & 0 & \textbf{0.01} & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
NavPosIntLimit & 8 & 5 & 3 & 5 & 5 & 8 & 12 & 3 & 3 & 12 & 12 & 12 \\
RxPitchCh & 2 & 2 & 2 & 2 & 2 & 2 & 2 & \textbf{1} & 2 & 2 & 2 & 2 \\
RxYawCh & 3 & 3 & 3 & 3 & 3 & 3 & 3 & 3 & 3 & 3 & 3 & 3 \\
MaxDescentRateDmpS & 12 & 30 & 10 & 18 & 30 & 12 & 25 & 9 & 10 & 25 & 25 & 25 \\
DescentDelayS & 15 & \textbf{10} & 15 & \textbf{10} & \textbf{10} & 15 & 15 & \textbf{10} & 15 & 15 & 15 & 15 \\
GyroLpfSel & 2 & 2 & 2 & 2 & 2 & 2 & 2 & 2 & 2 & 2 & 2 & 2 \\
NavCrossTrackKp & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 & 0.04 \\
RxGearCh & 4 & 4 & 4 & \textbf{5} & \textbf{5} & \textbf{5} & 4 & \textbf{5} & 4 & 4 & 4 & 4 \\
RxAux1Ch & 5 & 5 & 5 & \textbf{8} & \textbf{11} & \textbf{8} & 5 & \textbf{6} & 5 & 5 & 5 & 5 \\
ServoSense & \textbf{9} & 0 & 0 & 0 & 0 & \textbf{9} & \textbf{9} & 0 & 0 & \textbf{4} & 0 & \textbf{9} \\
AccConfSd & 0.06 & \textbf{0.04} & 0.06 & 0.06 & \textbf{0.04} & 0.06 & 0.06 & \textbf{0.02} & 0.06 & 0.06 & 0.06 & 0.06 \\
BatteryCapacity & 22 & 22 & 22 & 22 & 22 & 22 & 22 & \textbf{50} & 22 & 22 & 22 & 22 \\
RxAux2Ch & 6 & 6 & 6 & 6 & 6 & 6 & 6 & \textbf{4} & \textbf{11} & 6 & 6 & 6 \\
RxAux3Ch & 7 & 10 & 10 & 7 & 7 & 7 & 10 & 8 & 7 & 10 & 10 & 10 \\
NavPosKp & 0.33 & \textbf{0.2475} & \textbf{0.2475} & \textbf{0.2475} & \textbf{0.2475} & 0.33 & 0.33 & \textbf{0.2475} & 0.33 & 0.33 & 0.33 & 0.33 \\
AltLpf & 10 & 10 & 10 & \textbf{20} & 10 & \textbf{20} & 10 & 10 & \textbf{5} & 10 & 10 & 10 \\
Balance & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 \\
RxAux4Ch & 8 & 8 & 8 & \textbf{11} & 8 & \textbf{10} & 8 & \textbf{11} & 8 & 8 & 8 & 8 \\
NavPosKi & 0.008 & \textbf{0.012} & \textbf{0.012} & \textbf{0.012} & \textbf{0.012} & 0.008 & 0.008 & \textbf{0.012} & 0.008 & 0.008 & 0.008 & 0.008 \\
TiltThrottleFf & 0 & \textbf{0.1} & 0 & \textbf{0.25} & \textbf{0.1} & 0 & 0 & \textbf{0.07} & 0 & 0 & 0 & 0 \\
MaxYawRate & \textbf{7.67945} & 4.18879 & 2.0944 & \textbf{7.67945} & 5.23599 & \textbf{7.67945} & 2.0944 & 3.49066 & 2.0944 & 1.0472 & 2.0944 & 2.0944 \\
FwRollPitchFf & \textbf{0.25} & 0 & 0 & 0 & 0 & \textbf{0.25} & 0 & 0 & 0 & \textbf{0.3} & 0 & 0 \\
FwPitchThrottleFf & \textbf{0.1} & 0 & 0 & 0 & 0 & \textbf{0.1} & 0 & 0 & 0 & 0 & 0 & 0 \\
FwMaxClimbAngle & 0.261799 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 0.261799 & 0.523599 & 1.0472 & 1.0472 & 0.523599 & 0.523599 & 0.523599 \\
NavMaxAngle & \textbf{0.261799} & 0.349066 & \textbf{0.436332} & 0.349066 & 0.349066 & \textbf{0.261799} & 0.349066 & \textbf{0.261799} & 0.349066 & \textbf{0.698132} & 0.349066 & 0.349066 \\
FwSpoilerDecayPercentPs & 0.015 & 0.01 & 0.01 & 0 & 0 & 0.015 & 0.02 & 0 & 0 & 0.02 & 0.02 & 0 \\
FwAileronDifferential & \textbf{0.3} & 0 & 0 & 0 & 0 & \textbf{0.3} & 0 & 0 & 0 & 0 & 0 & 0 \\
KfAccUBiasVar & 3e-06 & 1e-06 & 3e-06 & 5e-06 & 0 & 0 & 2e-06 & \textbf{1e-05} & 3e-06 & 2e-06 & 2e-06 & 2e-06 \\
Config2Bits & - & - & - & - & - & - & - & - & - & 0 & 0 & - \\
MaxPitchAngle & 1.0472 & 1.0472 & \textbf{0.523599} & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & \textbf{0.523599} & 1.0472 & 1.0472 \\
MaxRollAngle & 1.0472 & 1.0472 & \textbf{0.523599} & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
YawLpfHz & \textbf{30} & 50 & 50 & 50 & 50 & \textbf{30} & 50 & 50 & 50 & 50 & 50 & 50 \\
NavHeadingTurnout & \textbf{0.698132} & 0.349066 & 0.349066 & 0.349066 & 0.349066 & \textbf{0.698132} & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 & 0.349066 \\
AltHoldThrCompDecayPercentPs & 0.001 & \textbf{0.02} & \textbf{0.025} & 0 & 0.001 & 0 & 0.001 & 0 & \textbf{0.02} & \textbf{0.01} & 0.001 & 0.001 \\
FwBoardPitchAngle & \textbf{0.087266} & 0 & 0 & 0 & 0 & \textbf{0.087266} & 0 & 0 & 0 & \textbf{0.069813} & 0 & 0 \\
MaxRollRate & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
MaxPitchRate & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 & 10.472 \\
CurrentScale & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 \\
VoltScale & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 \\
FwAileronRudderMix & \textbf{1} & 0 & 0 & 0 & 0 & \textbf{1} & 0 & 0 & 0 & 0 & 0 & 0 \\
FwAltSpoilerFf & \textbf{0.5} & 0 & 0 & 0 & 0 & \textbf{0.5} & 0 & 0 & 0 & 0 & 0 & 0 \\
MaxCompassYawRate & \textbf{1.5708} & 1.0472 & 1.0472 & 1.0472 & 1.0472 & \textbf{1.5708} & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 & 1.0472 \\
AccLpfSel & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\
YawRateKd & \textbf{0.000125} & 0.001125 & 0.001125 & 0.001125 & 0.001125 & \textbf{0.000125} & 0.001125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 & 0.001125 \\
ThrottleGainRate & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
RxAux5Ch & 9 & 9 & 9 & 9 & 9 & 9 & 9 & 9 & 9 & 9 & 9 & 9 \\
RxAux6Ch & 10 & 7 & 7 & 10 & 10 & 11 & 7 & 10 & 10 & 7 & 7 & 7 \\
RxAux7Ch & 11 & 11 & 11 & \textbf{4} & \textbf{4} & \textbf{4} & 11 & \textbf{7} & \textbf{6} & 11 & 11 & 11 \\
YawAngleKp & \textbf{2.25} & 3 & 3 & 3 & 3 & \textbf{2.25} & 3 & 3 & 3 & 3 & 3 & 3 \\
YawAngleKi & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 & 0.25 \\
YawAngleIntLimit & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 & 0.008727 \\
AltPosIntLimit & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & 0.5 & \textbf{0.75} & 0.5 & 0.5 & \textbf{0.75} & \textbf{0.75} & \textbf{0.75} \\
MotorStopSel & 0 & 0 & 0 & 0 & 0 & 0 & 0 & \textbf{0.002618} & 0 & 0 & 0 & 0 \\
AltThrottleCompLimit & 0.02 & 0.2 & 0.2 & 0.12 & 0.05 & 0.02 & 0.1 & 0.06 & 0.05 & 0.1 & 0.1 & 0.1 \\
VrsRoc & \textbf{50} & 30 & \textbf{50} & 30 & 30 & \textbf{50} & 30 & 30 & 30 & 30 & 30 & 30 \\
AhRocWindowMps & 5 & \textbf{15} & \textbf{20} & \textbf{30} & 5 & 5 & 5 & \textbf{15} & 5 & \textbf{15} & 5 & 5 \\
NavProxAltM & 5 & 3 & 4 & 3 & 3 & 5 & 3 & 2 & 1 & 5 & 5 & 3 \\
NavProxRadiusM & \textbf{10} & 1 & 3 & 2 & 1 & \textbf{10} & 3 & 2 & 1 & \textbf{30} & \textbf{25} & 3 \\
KfBaroVar & 50 & \textbf{20} & \textbf{100} & 50 & 50 & 50 & 50 & \textbf{20} & \textbf{20} & \textbf{20} & 50 & 50 \\
KfAccUVar & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 & 0.2 \\
FwStickScale & 4 & 4 & 4 & \textbf{2} & 4 & 4 & 4 & 4 & 4 & \textbf{5} & 4 & 4 \\
FwRollControlPitchLimit & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 & 0.785398 \\
AhThrottleMovingTrigger & \textbf{0.3} & 0.2 & 0.2 & \textbf{0.11} & 0.2 & \textbf{0.3} & 0.2 & \textbf{0.1} & 0.2 & 0.2 & 0.2 & 0.2 \\
NavFenceRadiusM & 100 & 100 & 100 & \textbf{200} & 100 & 100 & 100 & 100 & 100 & 100 & 100 & 100 \\
\bottomrule
\end{longtable}
## Notes

- Outlier detection: values > 3 MAD from the median are bolded.
- Unused/reserved parameters omitted.





