---
title: "MicroPython Jupyter in the Browser with ESP32-C3-DevKit-RUST-2"
date: 2025-10-17
showAuthor: false
series: ["WS00M"]
series_order: 1
tags: ["Workshop", "MicroPython", "Jupyter", "Browser"]
authors:
  - "daniel-paul"
showTableOfContents: false
showAuthor: false
summary: "Learn to program ESP32-C3-DevKit-RUST-2 microcontrollers using MicroPython and Jupyter notebooks directly in your browser, covering LED control, wireless communication, sensors, and MQTT."
---

Welcome to the workshop on MicroPython Jupyter in the browser! In this session, you will see how modern web technologies enable direct hardware programming without the need to install local development tools. You'll learn how to flash firmware, execute code interactively, and build IoT applications using only a browser and a USB connection.

## About the workshop

This workshop covers both fundamental and advanced MicroPython programming for ESP32-C3-DevKit-RUST-2 microcontroller through hands-on assignments:

<!-- no toc -->

**Setup** - Flash MicroPython firmware and understand the development environment

**Assignment 1: Blink** -- Control NeoPixel LED

**Assignment 2: Button Input** -- Read button presses and create interactive responses

**Assignment 3: ESP-NOW Communication** -- Implement wireless Morse code communication between two ESP32-C3-DevKit-RUST-2 devices

**Assignment 4: IMU Sensor and MQTT Communication** -- Read orientation data from an IMU and publish it to MQTT broker


## Prerequisites

### Hardware Prerequisites

- Computer running Windows, macOS or Linux
- Chromium-based browser (Google Chrome, Microsoft Edge, Opera, Brave, Vivaldi)
- ESP32-C3-DevKit-RUST-2 board (Provided by us)
- USB-C cable (data + power) compatible with the board

### Software Prerequisites

- Modern Chromium-based browser with WebSerial API support
- [Mosquitto](https://mosquitto.org/download/) message broker

### Effort

{{< alert icon="mug-hot">}}
**Estimated time: 120 min**
{{< /alert >}}

## Introduction

MicroPython is a lean implementation of Python 3 optimized for microcontrollers. It provides an interactive REPL (Read-Eval-Print Loop) and supports most Python standard library features, making embedded development accessible to Python programmers.

### Jupyter Notebook

Jupyter Notebook is a web-based interactive computing environment that allows you to create documents that contain live code, and narrative text. It is composed from a kernel, which is a program that executes the code, and a frontend, which is a user interface that allows you to interact with the kernel. The code is composed of cells, which can be executed independently or sequentially, either by clicking on the cell and pressing the run button or using a keyboard shortcut `Shift + Enter`. If the code executes a `while True` loop, it can be interrupted by clicking on the stop button in the toolbar.

### Why Jupyter MicroPython in the Browser?
Traditional embedded development requires installing toolchains, IDEs, and drivers. Browser-based Jupyter notebooks eliminate this setup by leveraging the WebSerial API, which allows web applications to communicate directly with serial devices. This approach offers several advantages:

- Zero installation: No local toolchain required
- Interactive development: Execute code cells individually and see immediate results
- Educational value: Clear separation of concepts into notebook cells
- Cross-platform: Works identically on Windows, macOS, and Linux
- Version control friendly: Notebooks can be easily shared and versioned

### How It Works
The browser connects to your ESP32-C3-DevKit-RUST-2 board via USB using the WebSerial API. Jupyter notebooks send Python code to the MicroPython REPL running on the device. The device executes the code and returns output, which displays in the notebook interface.

### Related documentation

- [MicroPython Documentation](https://docs.micropython.org/en/latest/)
- [ESP32 MicroPython Guide](https://docs.micropython.org/en/latest/esp32/quickref.html)
- [ESP-NOW Protocol](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_now.html)
- [ESP-NOW in MicroPython](https://docs.micropython.org/en/latest/library/espnow.html)

## Workshop

Without further ado, let's dive into the exciting world of ESP  microcontrollers and MicroPython! Please follow along as we explore the capabilities of this powerful platform.

* [Setup](setup/)
* [Assignment 1 - Blink](assignment-1/)
* [Assignment 2 - Button Input](assignment-2/)
* [Assignment 3 - ESP-NOW Communication](assignment-3/)
* [Assignment 4 - IMU Sensor and MQTT Communication](assignment-4/)

## Conclusion

You've learned to program ESP32-C3-DevKit-RUST-2 microcontroller using browser-based Jupyter notebooks, covering:

- MicroPython firmware flashing and interactive development
- GPIO control for LEDs and button input
- ESP-NOW wireless communication protocol
- IMU sensor data acquisition and processing
- MQTT protocol for IoT messaging

These skills form the foundation for building sophisticated IoT applications. The browser-based approach eliminates toolchain complexity while maintaining full access to MicroPython's capabilities.

## FAQ
- What kernel should I use?
  - Select `Embedded Kernel`.
- How do I connect my device to the Jupyter notebook?
  - Click on the ESP Control Panel, click `Connect` and select your device.
- Which of the devices is my ESP board?
  - The ESP board usually appears as `USB JTAG`.
- I cannot connect to a different Jupyter notebook.
  - Disconnect from the previous notebook and connect the new one.
- The notebook isn’t running my code, what should I do
  - In the ESP Control Panel, click `Disconnect device`, then reopen the notebook and connect again.
