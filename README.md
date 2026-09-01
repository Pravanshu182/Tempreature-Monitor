# Capstone Temperature Monitor

## Overview

The Capstone Temperature Monitor is a Linux-based temperature monitoring project developed using a custom Linux kernel character device driver and a user-space C++ monitoring application.

The project demonstrates communication between a Linux kernel module and a user-space application through a character device:

    User Application
          |
          v
    /dev/tempsensor
          |
          v
    Linux Kernel Driver
          |
          v
    Temperature Sensor Simulation

The application continuously reads temperature values, determines the current temperature state, displays the current time, temperature, and state, and reports state transitions.

---

## Features

- Custom Linux kernel character device driver
- Temperature sensor simulation
- Character device: `/dev/tempsensor`
- User-space C++ monitoring application
- Continuous temperature monitoring
- Temperature state classification
- Current date and time display
- State transition detection
- Temperature reset functionality
- Adjustable temperature drift
- Kernel module loading and unloading

---

## Temperature States

The temperature is classified into three states:

| Temperature | State |
|-------------|-------|
| Below 60°C | NORMAL |
| 60°C - 80°C | WARNING |
| Above 80°C | CRITICAL |

Example:

```text
Temperature: 52.0 C | State: NORMAL
Temperature: 67.0 C | State: WARNING
Temperature: 85.0 C | State: CRITICAL
