# OpenEruv

**Modernizing the Eruv – An Open-Source Community Project for Smarter Shabbat Boundaries**

## Table of Contents
1. [Introduction](#introduction)
2. [Why OpenEruv?](#why-openeruv)
3. [How It Works](#how-it-works)
4. [Project Goals](#project-goals)
5. [Technology Stack](#technology-stack)
6. [Getting Started](#getting-started)
7. [Contributing](#contributing)
8. [Project Roadmap](#project-roadmap)
9. [Community & Support](#community--support)
10. [License](#license)

## Introduction

**OpenEruv** is an open-source initiative aimed at modernizing the monitoring of eruvin by using cutting-edge technology. An eruv is a symbolic enclosure that allows observant Jews to carry items within a designated boundary on Shabbat. Traditionally, maintaining an eruv involves a labor-intensive weekly inspection to ensure that the wires are intact and compliant. **OpenEruv** aims to simplify this by creating a real-time, automated monitoring system that leverages sensor technology, mesh networking, and solar power.

This project is **open-source**, which means anyone with an interest in innovation, community, and technology is welcome to contribute. Together, we can modernize the eruv for the benefit of Jewish communities worldwide.

## Why OpenEruv?

1. **Modernize Traditional Practices**: Automate the weekly inspection process using technology, reducing labor and human error.
2. **Real-Time Alerts**: Get immediate notifications if the eruv is compromised, allowing for quick repairs.
3. **Community-Driven**: OpenEruv is developed by the community for the community. The contributions will help make it adaptable to diverse environments.
4. **Self-Sustaining**: Solar-powered monitoring means no reliance on power grids.

## How It Works

- **Tension Sensors**: Small tension sensors are attached at intervals along the eruv wire to measure the tension. If the tension drops below a threshold, it indicates a possible break.
- **Mesh Network**: The sensors are interconnected using **LoRa/Meshtastic** mesh networking, allowing long-range, low-power communication.
- **Central Gateway**: The mesh nodes communicate with a solar-powered central gateway, which sends out an alert using a SIM card (cellular connection) whenever a fault is detected.
- **Solar Power**: All components are powered by solar panels with rechargeable batteries, ensuring 24/7 functionality.

## Project Goals

- Develop a robust, low-maintenance system that can detect wire breakages in real-time.
- Create an affordable, open-source solution so that small communities can also implement automated eruv monitoring.
- Enable contributors to participate from anywhere in the world to help build and improve the system.
  
## Technology Stack

1. **Hardware**: 
   - Tension sensors
   - ESP32 microcontrollers
   - Solar panels with lithium-ion battery storage
   - SIM-enabled gateway (ESP32 + GSM module)

2. **Communication Protocol**: 
   - **LoRa/Meshtastic** for the mesh network
   - GSM for the central gateway to send out alerts

3. **Software**:
   - Firmware for ESP32 microcontrollers (C++/Python)
   - Web or mobile app (Optional) for monitoring the system
