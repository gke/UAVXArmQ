# UAVXArmQ — Firmware Releases

UAVXArmQ is a constrained-C flight-controller firmware for STM32F4 fixed-wing and
multirotor targets.

It is a first-party fork in the UAVX line, derived from UAVX by Prof. Greg Egan
(© 2008) and the original UAVX V3.15 by Ing. Wolfgang Mahringer (© 2007), and is
distributed under the GNU General Public License v3.

This repository publishes prebuilt firmware images only — no source code.

## What's new

- Unified float32 parameter set (all 128 parameters; no uint8 split)
- Quaternion attitude and navigation; revised rate and tuning telemetry
- Fixed-wing throttle cut, control-surface authority and commissioning defaults
- Reassigned RC channels: arming/nav qualification, Dive (rapid descent),
  Trace (diagnostic capture), RateGain (in-flight rate scaling)
- Magnetometer warm-up retry

## Firmware

| Target | Files |
|--------|-------|
| BLUEBERRYF405 | BLUEBERRYF405Q_r0.bin |
| DEVEBOXF4 | DEVEBOXF4Q_r0.bin |
| FLYINGRCF4WINGMINI | FLYINGRCF4WINGMINIQ_r0.bin |
| MATEKF411WING | MATEKF411WINGQ_r0.bin |
| SPEEDYBEEF405WING | SPEEDYBEEF405WINGQ_r0.bin |
| UAVXF4V3 | UAVXF4V3Q_r0.bin UAVXF4V3Q_r67.bin |
| UAVXF4V4 | UAVXF4V4Q_r0.bin |

## Loading the firmware

Load a prebuilt image either:

- via **UAVXGS**, the ground station's *Flight-Controller firmware load*, or
- via **DFU** — put the board in DFU mode first (hold BOOT0, tap reset,
  release), then flash:

  ```
  dfu-util -a 0 -s 0x08000000:leave -D <image>.bin
  ```

## Supported boards

UAVXF4V3 / UAVXF4V4, DevEBox F4, SpeedyBee F405 Wing, FlyingRC F4 Wing Mini,
Blueberry F405, MatekF411Wing.

## History

`HISTORY.md` preserves the original UAVX RCGroups development thread —
historical reference only, not current documentation.

## License

GNU General Public License v3 — see the source headers for the copyright and
attribution notices.

The repo intentionally holds only the compiled images — no source, build
intermediates, wiki, or scripts are published.
