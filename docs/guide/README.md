---
title: User Guide
version: 1.6.0
---

# User Guide

## Concepts

XOD language objects and processes described in detail.

- [Program structure](./program-structure/)
- [Data types](./data-types/)
- [Linking rules](./linking-rules/)
- [Execution model](./execution-model/)
- [Variadic nodes](./variadics/)
- [Generic nodes](./generics/)
- [Buses](./buses/)
- [Errors](./errors/)

## Making your own nodes

The most straightforward way to extend XOD and add support for new hardware.

- [Creating nodes for XOD in XOD](./nodes-for-xod-in-xod/)
- [Creating analog sensor driver nodes](./analog-sensor-node/)
- [Documenting nodes](./documenting-nodes/)
- [Creating nodes for XOD in C++](./nodes-for-xod-in-cpp/)
- [Dealing with state in C++](./cpp-state/)
- [Dealing with time in C++](./cpp-time/)
- [Migrating C++ nodes to v0.35](./migrating-to-v035/)
- [Creating variadic patch nodes](./creating-variadics/)
- [Passing variadic inputs through](./variadic-pass/)
- [Creating generic patch nodes](./creating-generics/)
- [Defining custom types](./custom-types/)
- [Creating records](./records/)
- [Wrapping class-based Arduino libraries](./wrapping-arduino-libraries/)
- [Testing patches](./testing-patches/)

## XOD Cloud

Cloud services for IoT development.

- [Getting started with feeds](./getting-started-with-feeds/)
- [Multiple time series](./multiple-time-series/)

## XOD Graphics

- [Graphics library](./graphics-library/)
- [Loading images](./graphics-images/)

LCD and OLED graphic displays:

- [ST7735 display](./st7735-display/)
- [SSD1306 display](./ssd1306-display/)

## Case studies

- [Working with servo motors](./servo/)
- [Working with text displays](./text-lcd/)
- [Digital clock example](./rtc-example/) — working with RTC modules
- [Temperature log example](./sd-log-example/) — logging to SD card and visualizing data
- [Simple traffic light example](./simple-traffic-light/) — doing things sequentially
- [NFC smart lock](./nfc-lock-example/) — working with RFID/NFC module and text LCD
- [Coloring WS2812 LEDs](./ws2812-neopixel/) — working with WS2812 RGB LEDs, also known as NeoPixel

Interfaces and protocols:

- [Controlling LEDs via UART](./uart-led-control) — exchanging text-based data between two boards
- [I²C communication basics](./i2c/)

IoT and network communication:

- [Quick setup of W5500 Ethernet Shield for Internet and LAN communication](./w5500-connect/)
- [Advanced setup of W5500](./w5500-advanced/)
- [Connecting to Internet with ESP8266-based MCUs](./esp8266-connect/)
- [Fetching data from web API’s with HTTP GET requests](./http-get/)
- [Reading JSON data](./reading-json-data/)

<a name="projects-and-libraries"><!-- Old anchor name --></a>

## Development

How to create, manage, and share programs in XOD.

- [Working on projects](./projects/)
- [Debugging programs](./debugging/)
- [Sharing Internet from PC](./tethering-inet/)
- [Using libraries](./using-libraries/)
- [Creating libraries](./creating-libraries/)
