# Miele Scout RX2 — Flipper Zero Remote

Custom Flipper Zero app for controlling the Miele Scout RX2 robot vacuum via infrared.

## Install

Copy `dist/miele_scout.fap` to your Flipper Zero SD card:

```
SD Card/apps/Infrared/miele_scout.fap
```

Open it from **Apps > Infrared > Miele Scout RX2**.

## How it works

The app has two modes. Press **Back** to switch between them.

### Drive mode

Use the Flipper's d-pad to steer the robot in real time:

- **Up / Down / Left / Right** — move the robot
- **OK** — start cleaning

Hold the Flipper vertically (IR port pointing at the robot). The d-pad directions match the robot's movement. Release the button to stop — there's no drift.

### Menu mode

Scroll through commands with **Up / Down**, press **OK** to send:

- **POWER** — turn on/off
- **BASE** — send robot to charging base
- **PLAY/PAUSE** — start or pause cleaning
- **WIFI** — WiFi pairing
- **TIMER** — set timer
- **PROGRAM** — change cleaning program
- **CLIMB** — toggle obstacle climbing height (HI/LO)
- **MUTE** — toggle sound feedback (ON/OFF)
- **OK** — confirm selection on robot display

### Exit

Long-press **Back** to close the app.

## Build from source

Requires [ufbt](https://github.com/flipperdevices/flipperzero-ufbt):

```
pip install ufbt
ufbt
```

Output lands in `dist/miele_scout.fap`.

## Compatibility

Built for Flipper Zero official firmware. Uses NEC IR protocol (address 0x01). Should work with any Miele Scout RX2 unit that came with the standard IR remote.
