---
geometry: margin=1in
fontsize: 10pt
---
# UAVXGS Ground Control Station #

UAVXGS is the Python 3 / PyQt5 ground control station for UAVXArmQ. It runs on Linux, macOS, and Windows. Refer to the GCS Guide (in the GCS kit `wiki/docs/`) for full window-by-window documentation.

## Voice Feedback ##

Selectable voice feedback is available via the Speech dropdown in the status bar (Off, Errors, Warnings, Info, All). This allows you to keep your eyes on the aircraft in flight.

## Connecting ##

1. Connect the FC via USB.
2. Select the serial port from the **COM:** dropdown (auto-detected).
3. Baud rate is 115200.
4. Click **Connect**. The status indicator turns green when linked.

On connection the GCS reads all 128 parameters from the FC. The **Revision** label at the top of the Parameter Window shows the current firmware version.

# Main Window #

The main window displays:

- **Attitude Sphere** — 3D artificial horizon with compass rose, pitch/roll and heading.
- **Altitude Display** — Kalman-filtered baro+acc altitude in metres with ROC.
- **State & Battery** — flight state, nav state, waypoint, alarm, voltage, current, consumed mAh.
- **Controls** — throttle, roll, pitch, yaw bargraphs.
- **IMU** — angles, rates, accels, MPU temperature, acc confidence.
- **Navigation** — next waypoint, bearing, distance, cross-track, wind, magnetic variation.
- **GPS** — lat/lon, ground speed, satellites, HDOP, fix type.
- **Flags** — Armed, InFlight, AngleMode, AltHold, GPS, HomeSet, etc.

# Parameters #

Open using the **Params** button in the toolbar.

There is a single parameter page with grouped categories (Basic, Gains, Rates, Altitude, Navigation, Misc, Tuning) selectable by tabs. All 128 parameters are stored and transmitted as `float32`. Display values are converted to/from FC-native units automatically.

### Operations ###

- **Read** — reads all parameters from the FC.
- **Write** — writes all changed parameters to the FC.
- **Save** — saves the current parameter set to a `.af` file.
- **Load** — loads a `.af` file into the table (not written to FC until Write).
- **Commit** — writes, conditions, flashes, and resets the FC.

IMPORTANT: Any programming of the aircraft should be done with props OFF. Some changes to the aircraft type, Rx type/mode or Emulation mode may require a reset so that the hardware can be reconfigured SAFELY.

If there is no response to GCS commands, check the LEDs to see if they are all flashing. If they are, power cycle the board only after you have checked that your aircraft matches the one selected.

## A Reminder on Failsafes ##

UAVX will do whatever you have set on your Rx failsafes. Carefully set them to the action you desire. Usually this is sticks neutral and RTH selected.

# Navigation #

Open using the **Nav** button in the toolbar.

The navigation window displays an OpenStreetMap with the aircraft position, home point, and waypoints. Missions may be loaded, saved, and uploaded to the FC.

Navigation including hold is disabled for the first approximately 15 seconds of flight. Selecting Nav Mode other than PIC will result in an autoland. You can abort this by reversing the switch action.

## General ##

Missions may be accessed as files using the Load and Save buttons. An image of the current map is also saved when using the Save button.

Changes to the mission on the map must be uploaded to the aircraft using the Write button. The current mission stored in the aircraft (if any) is downloaded using the Read button.

## Emulation ##

You should use **Emulation Mode** to help you become familiar with the mission planning and the effect of the various Nav Modes.

When no FC is connected, the GCS auto-starts emulation mode. The FC simulator generates synthetic GPS and flight data with a light breeze to the NE. The Nav window shows a default mission that can be edited and tested without hardware.

**REMOVE YOUR PROPELLORS WHEN USING EMULATION**. The software should disarm motor function when emulation is selected but I don't trust software so neither should you.

## First Emulated Flight ##

Select the Read button to upload any mission currently stored in UAVX. In Emulation Mode you should see a simple mission displayed.

**WAIT** until the "Home Set" status box is lit signifying GPS lock has occurred and the origin has been acquired.

Increase throttle and "fly" to around 15M. Slowly reduce the throttle to 45% which is hover. You should see the ROC drop to close to zero at which point the altitude hold will engage.

Select Navigate on the Nav Mode switch. You should now see (and hear) the aircraft start to traverse the mission.

Try selecting RTH then re-selecting Navigate. Note you must go to Hold then back to Navigate otherwise RTH will continue. Currently the mission is restarted not resumed where it left off.

## More Advanced ##

Most of the usual features you would expect are available:

  * The types of waypoints and some edits are available with right mouse click — the position of the mouse when you click will be the position of the waypoint.
  * The up/down buttons in the mission data box may be used to edit default values, change the waypoint sequence or delete individual waypoints.
  * Conditional waypoint sequences/loops are not currently available.

The waypoint types are currently:

  * VIA — where the aircraft pauses (T) at a waypoint attempting to stay within the proximity radius and altitude limits. If the time is set to zero then the aircraft must go through the waypoint within the proximity radius but not necessarily the altitude.
  * ORBIT — orbits the waypoint at the radius (R) with a velocity (V). UAVX will point a camera at the waypoint.
  * PERCH — lands at the waypoint then takes off and resumes mission.
  * Set POI — this is not a waypoint as such just a point that the aircraft will point to for the rest of the mission or until another Set POI is encountered.
  * SURVEY — this allows you emit a pulse of a fixed width on the Aux1 pin repeated at periodically commencing at the next waypoint.

Although not displayed RTH is always the default last waypoint. If there is no mission then selecting Navigate results in RTH.

If you do not designate a POI then the normal Turn To WP or hold heading configuration applies.

If the aircraft is currently at a much higher altitude than that desired upon reaching a waypoint it is possible to achieve a much more rapid descent. Rapid vertical descents in rotorcraft can result in a condition called Vortex Ring State (VRS). We attempt to avoid this condition by forcing the aircraft into forward orbiting flight until it is close to the desired altitude at which time the descent rate will slow to that set in the parameters. This strategy is enabled using the "Normal/Rapid" checkbox. If you are flying manually you should have a small amount of forward motion when descending rapidly otherwise you may just go all the way in!

http://en.wikipedia.org/wiki/Vortex_ring_state

Any changes to the mission do not become effective until you **select Write**. You should always select Read immediately after to satisfy yourself that the mission appears OK.

## Go To ##

If the Go To checkbox is checked then a right click of the mouse will generate a 1 point mission. This allows you to fly to a designated point dynamically with no control inputs. Again you must select Write to upload the mission change.

# DFU Flasher #

Open using the **Flash** button in the toolbar.

Uploads firmware to the STM32 flight controller via the UART DFU bootloader. No external programmer (ST-Link) required. Select the firmware `.bin` file, put the FC in DFU mode (hold boot button, power cycle, or click "Enter DFU"), and click Flash.

# Calibration #

Open using the **Calib** button in the toolbar.

Provides guided calibration for accelerometer, gyroscope, and magnetometer with live sensor readback and progress indication. All calibration buttons are disabled when the aircraft is armed.

# Misc — Raw Packet Monitor #

Open using the **Misc** button in the toolbar.

A scrolling table showing every received packet by tag, name, direction, and hex body. Useful for protocol debugging and bandwidth analysis.

# Finally #

It is important to familiarise yourself with what happens when you change the Nav Mode switch selection. Some of the changes may not be exactly as you expect and it is better to see the effect under emulation.
