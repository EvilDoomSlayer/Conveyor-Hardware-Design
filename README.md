# Conveyor-Hardware-Design

This repository contains the mechanical design files for the **Luggage Classification Conveyor** system. It is a submodule of the main firmware repository.

## Overview

This collection of files defines the physical structure of the automated sorting system. It includes the chassis for the conveyor belt, mounts for the servo motors, housings for the sensors (IR, Magnetic, Load Cell), and the diversion gates used to sort the luggage.

## Directory Structure

* **/SolidWorks**: Contains the source CAD files (`.SLDPRT` and `.SLDASM`) for modification and assembly viewing.
* **/STL**: Ready-to-print files for 3D printing.
* **/DXF**: Vector files intended for laser cutting (if applicable) or reference.

## Bill of Materials (Mechanical)

To assemble the physical conveyor, you will need the printed parts found in the `/STL` folder, plus the following hardware:

* **Actuators**:
    * 1x DC Motor (Standard geared TT motor or similar).
    * 2x SG90 Micro Servos (for the sorting arms).
* **Sensors**:
    * 1x E18-D80NK IR Proximity Sensor.
    * 1x Load Cell (1kg or 5kg depending on scale) + HX711 Board.
    * 1x KY-024 Linear Magnetic Hall Sensor.
* **Fasteners**:
    * Assorted M3 screws and nuts.
    * Conveyor belt material (Fabric or rubber strip).

## Assembly Notes

1.  **Servo Calibration**: Before permanently mounting the servo arms, ensure the servos are set to their neutral positions using the calibration tools found in the `Conveyor-Tools` repository.
2.  **Load Cell Mounting**: Ensure the load cell is mounted with the correct orientation (arrow pointing down) and that the weighing platform does not touch the base chassis to ensure accurate readings.
3.  **Sensor Placement**:
    * The **IR Sensor** must be placed at the start of the belt.
    * The **Magnetic Sensor** should be placed under the belt along the "Light Luggage" path.
    * The **Load Cell** is located at the end of the sorting path.

## Software Used

* **SolidWorks**: For 3D modeling.
* **Ultimaker Cura** (or similar): For slicing STL files for printing.
