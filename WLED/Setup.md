# WLED Configuration and Setup

## Overview

WLED serves as the primary control platform for the lighting system. It provides wireless control, effect management, segmentation, preset storage, and integration with third-party software through the local network.

## Standard WLED Installation

### Requirements

* ESP32 Development Board
* USB Data Cable
* Internet Connection
* WLED Web Installer

### Installation Procedure

1. Connect the ESP32 to a computer using a USB data cable.
2. Open the WLED Web Installer.
3. Install any required USB drivers if the ESP32 is not detected.
4. Select the detected ESP32 device.
5. Put the ESP32 into bootloader mode if required.
6. Start the installation process and wait for completion.
7. After installation, connect to the temporary Wi-Fi network created by WLED.
8. Open the WLED setup page and configure local Wi-Fi credentials.
9. Allow the ESP32 to connect to the home network.

Once connected, WLED can be accessed through:

* Local IP Address
* WLED Mobile Application
* Web Browser Interface

## LED Configuration

The system uses two independently controlled LED outputs.

### Output Configuration

| GPIO Pin | Function                  |
| -------- | ------------------------- |
| GPIO 4   | LED Segment 1 Data Output |
| GPIO 16  | LED Segment 2 Data Output |

Each LED data line is protected using a 220Ω series resistor.

## Segmentation

Segmentation is a key feature of the project.

By dividing the LED strip into multiple segments, different sections can display independent effects, colors, brightness levels, and animations simultaneously.

This functionality is especially useful when integrating WLED with external software such as:

* LedFX
* SignalRGB
* Resolume Arena

Proper segmentation significantly improves effect quality and flexibility.

## Preset Management

Custom presets were created for different room environments and use cases.

Examples include:

* Ambient Lighting
* Relaxation Modes
* Music Reactive Effects
* Screen Ambience
* Dynamic Color Effects

Presets can be activated through:

* WLED Web Interface
* WLED Mobile Application
* Third-Party Software
* Local Network Commands

## Network Control

Once connected to the home Wi-Fi network, the lighting system becomes accessible from any device on the same network.

Control options include:

* Smartphone
* Tablet
* Desktop Computer
* Automation Software
* Visualization Software

The local IP address serves as the primary endpoint for software integrations.

## User Interface

The WLED interface provides:

* Real-time brightness control
* Color selection
* Effect selection
* Segment management
* Preset management
* Device configuration
* Network configuration

The interface allows rapid switching between different lighting modes without requiring firmware modifications.
