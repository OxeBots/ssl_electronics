# SSL Electronics - Oxebots

Electronics design for the RoboCup Soccer Small-Size League (SSL).

## System Architecture

*   **Main Board:** ESP32-based controller board.
*   **Power Board:** Power distribution and battery protection.
*   **Kicker Board:** Board that drives the solenoid through a capacitor bank charged up to 200V.

## Repository Structure

*   `/pcbs`: KiCad boards project files.
*   `/Libraries`: Custom symbols, footprints, and 3D models.
*   `/exported`: STEP and 3D exports.
*   `/datasheets`: Component documentation.

## Core Components

*   **Toolchain:** KiCad 9.0+
*   **MCU:** ESP32 38-pin
*   **RF:** NRF24L01+
*   **Sensors:** GY-85 (IMU), AS5600 (motor encoder), VL53L5X (ToF sensor)
*   **Motors:** BL48250 motor with driver board (for 24V).
*   **Solenoid:** 25X50TL (for 24V)

## Configuration

To resolve library dependencies in KiCad, you must configure the `OXEBOTS_SSL_LIB_DIR` path variable:

1.  Open KiCad.
2.  Go to **Preferences** > **Configure Paths...**
3.  Add a new entry (+ symbol):
    *   **Name:** `OXEBOTS_SSL_LIB_DIR`
    *   **Path:** Path to the `Libraries` folder in your local machine.

This ensures all schematic symbols, footprints, and 3D models are correctly linked.
