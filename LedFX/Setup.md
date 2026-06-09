# LedFX Integration

## Overview

LedFX was integrated into the project to provide advanced audio-reactive lighting effects based on direct audio capture from the computer.

Unlike WLED-SR, which relies on a physical microphone, LedFX processes audio directly from the PC, resulting in cleaner and more accurate synchronization with music and media playback.

## Motivation

While WLED-SR offers excellent standalone audio-reactive capabilities, microphone-based systems can be affected by:

* Environmental noise
* Room acoustics
* Speaker placement
* Background sounds

LedFX eliminates these limitations by using the computer's audio stream as the input source.

This approach provides:

* More accurate beat detection
* Cleaner frequency analysis
* Improved synchronization
* Consistent performance regardless of room conditions

## System Architecture

Audio Playback on PC
↓
LedFX Audio Processing
↓
Wi-Fi Network
↓
WLED Device (ESP32)
↓
WS2812B LED Strips

## Integration Process

### Device Discovery

The WLED controller was connected to the local Wi-Fi network.

LedFX automatically detected the WLED device through its local IP address, allowing communication between the software and the lighting controller.

### Device Configuration

The following information was configured:

* Device Name
* Local IP Address
* LED Count
* Segment Mapping
* Effect Settings

Once configured, LedFX could control the LEDs in real time through the network.

## Audio Processing

LedFX captures audio directly from the computer and performs real-time analysis.

The software processes:

* Bass frequencies
* Mid-range frequencies
* High frequencies
* Beat detection
* Dynamic amplitude changes

The analyzed audio data is then converted into lighting effects and transmitted to WLED.

## Effect Configuration

Multiple effect types were tested, including:

* Spectrum Visualizers
* Frequency Bars
* Beat Detection Effects
* Wave Animations
* Color Pulse Effects
* Dynamic Music Visualizations

Different effect configurations were evaluated to determine which produced the most immersive lighting experience.

## Advantages Over Microphone-Based Systems

### WLED-SR

* Uses external microphone input
* Requires gain tuning
* Sensitive to environmental noise

### LedFX

* Uses direct PC audio
* No microphone required
* Consistent audio analysis
* Improved synchronization accuracy

Both solutions have advantages depending on the use case and were retained as separate operating modes within the project.

## Performance

LedFX provided highly responsive visualizations during:

* Music playback
* Video streaming
* Gaming sessions
* General desktop use

The direct audio processing approach resulted in smoother and more predictable lighting behavior compared to microphone-based audio capture.

## Lessons Learned

* Direct audio capture provides more accurate audio-reactive effects.
* Network stability is important for maintaining smooth LED updates.
* Proper LED segmentation improves visualization quality.
* Different effect styles perform better depending on the content being played.
* LedFX complements WLED-SR rather than replacing it.

## Result

LedFX successfully expanded the system's capabilities by enabling high-quality audio-reactive effects based on internal computer audio, creating a more immersive and responsive ambient lighting experience.
