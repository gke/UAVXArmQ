# HISTORY.md — UAVX Community Thread (RCGroups #1093510)

> **NOTICE: This document is HISTORICAL ONLY.**
> It preserves the original RCGroups thread content for reference.
> For current firmware documentation, configuration, and development references,
> consult the other files in this repository.

*Thread: "New Quadrocopter and Tricopter UAVP updated with GPS and more - UAVX!"*
*OP: gke (Prof. Greg Egan), Aug 10, 2009*

---

## Original Post (First Post by gke)

### Some History

The public release of UAVP V3.05 by Dr Wolfgang Mahringer was 15 March 2007 and as such was one of the first. UAVXPIC was based on UAVP V3.15 running on the Black Board with the PIC876. The PIC876 processor was replaced by the PIC2520 but both are now like the dinosaurs. Nonetheless they still flew well with a 200Hz main loop, discrete gyros and accelerometers on the bigger frames.

The originating thread from which this thread is derived is: UAVP Info Thread (t=811550). The UAVXArm prototype first ran on Arm around December 2008 and was released based on STM32F407 in August 2009. The F1 Arm which was in wide use later, by others, was always a dead end. There was lots of activity back then including Mikrokopter also with pretty much all of the Navigation and other functionality that we expect now but a decade ago. The big change was the Racers but then again Warthox was showing the way a long long way back.

### UAVXArm

The UAVXArm32F4 V4 board is now available to order from Ken at QuadroUFO.

The V4 uses the:
- STM32F407RG CPU
- MPU6000 IMU
- MS5611 Barometer
- HMC5983 Magnetometer
- AT45DB641E 64Mbit FLASH for logs + Arm.
- All sensors use SPI.

The V4, at this date, is probably the smallest full-house F4 board out there and has been flown on regular 600 scale hexacopters down to nano quads. In the latter case a daughter board also available from QuadroUFO provides 1/2S support for up to 6 brushed motors.

While designed for UAVX the V4 board is a simple porting target for other flight codes (Cleanflight et al., AutoQuad etc.) which have now adopted, or support, the same sensor package. MultiWii 2.3 was ported and flown.

Google has withdrawn support for project code uploads so monitor gitHub for firmware updates. Always archive your known working versions.

### UAVX Functionality

UAVX continues to support the functions and failsafe features it has had for almost a decade including return to home and waypoint navigation. Recent additions include:
- VRS avoidance
- Inflight vibration monitoring using DFTs
- Bad motor/ESC diagnostics
- SyncPWM and oneShot although some/many remain unconvinced
- FrSky telemetry and MAVLink telemetry intended principally for minimOSD
- Representative physics for emulation mode
- Single UAVXGUI groundstation application
- WS2812 LED support for pretty lights

### Startup Documentation

The startup document should get you in the air. All electrically powered devices are potentially dangerous so pay particular attention to notes on safety.

Detailed information, much of which was produced by Jim aka Jesolins, may be found in the following post. The Wikis, partially recovered from the now dead Google Projects are now on gitHub. The original uavp-mods wikis are also in the gitHub archive.

### Release Date

UAVX was first released 15th August 2009 Australian EST.

### Caveat

We do this for FUN not money and entirely in our own free time so we are permanently in Beta Test. Choosing to be involved in this "testing" is entirely at your own risk. We welcome constructive considered comments on how we can improve UAVX as part an overall community effort which this and other RCG threads are intended to be.

### Acknowledgment & Disclaimer

We wish to acknowledge the pioneering work of Dr Wolfgang Mahringer the author of UAVP. Any and all use of material on this thread including in particular the use of UAVX and its support software is entirely at your own risk — see the GNU Licence provisions.

---

## Board Images

- **UAVXArm32F4 V4** — STM32F407RG, MPU6000, MS5611, HMC5983, 64Mbit FLASH (wiki/graphics/Uavx-nanoV4.png)
- **UAVXArm32F4 V4 Pinouts** (wiki/graphics/UAVXArm32F4_V4Pinouts.JPG)

---

## Community

The UAVX/UAVP community on RCGroups spans thousands of posts across two long-running threads (UAVX: 672 pages, UAVP: 234 pages). The community was too large to list individually. Key contributors are acknowledged in the original post above.

---

*Source: RCGroups #1093510 — "New Quadrocopter and Tricopter UAVP updated with GPS and more - UAVX!" (derived from UAVP #811550)*