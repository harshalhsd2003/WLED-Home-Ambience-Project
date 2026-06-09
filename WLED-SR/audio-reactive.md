# WLED Sound Reactive (WLED-SR)

## Overview

To enable audio-reactive lighting effects, the project uses WLED Sound Reactive (WLED-SR), a modified version of WLED that adds microphone-based audio processing and music visualization capabilities.

This allows the LED strips to react dynamically to music, voice, and environmental sounds in real time.

## Motivation

While standard WLED provides a large collection of visual effects, it does not include advanced microphone-based audio analysis.

WLED-SR was selected to add:

* Real-time music visualization
* Beat-reactive effects
* Frequency-based animations
* Dynamic ambient lighting synchronized with sound

## Firmware Availability Challenge

During development, the original WLED-SR installation resources were no longer readily available through the standard installation methods used for WLED.

As a result, archived firmware files and older project resources had to be located manually.

The firmware was then installed locally instead of using the standard web-based installation process.

This required additional research into firmware compatibility and manual flashing procedures.

## Installation Procedure

### Firmware Preparation

1. Locate a compatible WLED-SR firmware release.
2. Download the required firmware files.
3. Verify compatibility with the ESP32 hardware.

### Flashing Process

1. Connect the ESP32 to the computer via USB.
2. Use a local flashing tool to upload the WLED-SR firmware.
3. Wait for the firmware installation to complete.
4. Connect to the temporary Wi-Fi network created by the device.
5. Configure local Wi-Fi credentials.
6. Access the device through its local IP address.

After installation, the general setup and configuration process remains similar to standard WLED.

## Audio Hardware

### Microphone Module

MAX9814 Automatic Gain Control Microphone Amplifier

The MAX9814 microphone module was selected because of its built-in amplification and adjustable gain characteristics, making it suitable for audio-reactive lighting applications.

### Wiring

| MAX9814 Pin | ESP32 Connection           |
| ----------- | -------------------------- |
| VCC         | 5V                         |
| GND         | GND                        |
| OUT         | Configured Audio Input Pin |

The microphone shares the same regulated 5V power supply as the ESP32.

## Audio Configuration

Achieving accurate audio-reactive behavior required extensive tuning and experimentation.

Several parameters influence the final visual response:

### Microphone Gain

The gain adjustment on the MAX9814 significantly affects:

* Sensitivity
* Noise floor
* Response to music
* Dynamic range

Improper gain settings can result in:

* Excessive noise
* Constant triggering
* Weak visual response

### Effect Sensitivity

WLED-SR provides configurable sensitivity settings that determine how aggressively effects respond to incoming audio signals.

Finding the optimal balance required multiple rounds of testing with:

* Music playback
* Different volume levels
* Environmental noise
* Various audio-reactive effects

## Optimization Process

The final configuration was achieved through iterative testing and adjustment.

Key areas optimized included:

* Microphone placement
* Gain settings
* Audio sensitivity
* Effect selection
* Overall responsiveness

The resulting setup provides a balanced response that works effectively for both music listening and ambient room lighting.

## Lessons Learned

* Audio-reactive lighting performance depends heavily on microphone tuning.
* Hardware gain and software sensitivity must be adjusted together.
* Different music genres may require different tuning preferences.
* Proper microphone placement can significantly improve effect quality.
* Firmware availability can become a challenge when community projects are no longer actively maintained.

## Result

The WLED-SR integration successfully enabled real-time audio-reactive lighting effects, transforming the LED system into a dynamic visualization platform capable of responding to music and ambient sound.
