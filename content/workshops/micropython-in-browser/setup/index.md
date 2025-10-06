---
title: "Setup"
date: 2025-10-17T00:00:00+01:00
showTableOfContents: false
series: ["WS00M"]
series_order : 2
showAuthor: false
---

## Setup

Let's start by flashing MicroPython firmware.

### Flashing MicroPython Firmware

1. Connect your ESP32-C3-DevKit-RUST-2 board to your computer via USB cable
2. Open your Chromium-based browser and navigate to the [website](https://xdanielpaul.github.io/jupyter-lite-micropython/lab/index.html)
3. Open the sidebar folder, navigate to `examples/Assignment 1.ipynb` and open the notebook
4. When prompted with selecting kernel, select `Embedded Kernel`
5. On the ESP Control Panel select `Connect device` and select ESP device from the options (usually USB JTAG)
6. On the same ESP Control Panel select `Flash Device` and `Flash Selected Firmware` - this will flash MicroPython to your device

Your device is now ready to run MicroPython code.

You can now proceed to the next [assignment](../assignment-1)!
