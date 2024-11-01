# Enhanced Radar System

**Version:** 0.0.0  
**Date:** 11/01/2024  
**Author:** SlammingProgramming  

## Overview
Welcome to the Enhanced Radar System! This script builds on the foundational work of existing radar systems and introduces a plethora of new features aimed at significantly boosting your situational awareness in Space Engineers. It retains the core functionality of utilizing turret targeting while incorporating advanced capabilities for improved radar visualization, networking, and user customization.

## Key Features

### Advanced Targeting and Visualization
- **3D Radar Display:** A visually refined radar system that plots targets on a 3D plane, mirroring the radar interface found in games like Elite Dangerous.
- **Elevation Indicators:** Vertical lines provide a clear indication of the target's elevation relative to your ship, enhancing depth perception during engagements.
- **Dynamic Target Highlighting:** Targets are dynamically highlighted based on threat level and distance, improving quick decision-making in combat situations.

### Enhanced Target Sharing
- **Antenna Network Integration:** Seamless target sharing across multiple ships equipped with antennas. If one ship detects a target, all ships within antenna range will see the target on their radar.
- **Lock Status Display:** Targets locked by WHAM or LAMP are prominently displayed for strategic awareness.

### User-Friendly Setup and Customization
- **Setup Instructions Simplified:** Streamlined setup process with clear, concise instructions to get you up and running quickly.
- **Customizable Appearance:** Modify radar display settings directly in the programmable block’s Custom Data. Change colors, sizes, and display formats to suit your preferences.
- **Multi-Screen Support:** Effortlessly create a large radar display by configuring multiple LCD panels, giving you a panoramic view of your surroundings.

### Improved Control and Responsiveness
- **Reference Controller Configuration:** Specify a primary ship controller for radar orientation, enhancing accuracy during maneuvering.
- **Sensor Integration:** Use onboard sensors to automatically detect nearby targets, adding another layer of situational awareness.

### New Functionalities
- **Extended Radar Range Control:** Set radar range dynamically or revert to turret maximum range easily via command arguments.
- **Additional Argument Options:** Enhanced command arguments for more granular control:
  - **range [number]:** Set radar range in meters.
  - **threat [level]:** Filter displayed targets based on threat levels (e.g., 1 for enemy, 2 for neutral, etc.).
  - **refresh:** Reprocess settings to apply changes made in the Custom Data.

### Compatibility and Integration
- **Support for Custom Turrets:** Fully compatible with custom turret control blocks, expanding usability.
- **Integration with Existing Scripts:** Compatible with other radar scripts and IFF systems, enabling broader interoperability within your fleet.
- **Mod Support:** Enhanced compatibility with modded items and longer-range turrets.

## Setup Instructions

### Required Steps
1. Upload this script to the programmable block of your ship.
2. Add turrets and custom turret control blocks as needed.
3. Name text panels or blocks with text surfaces containing the word **Radar** for display.
4. Configure the desired text surface within the block's Custom Data.

### Optional Steps
- Add one or more ship controllers (Cockpits, Flight Seats, or Remote Controls) to specify radar orientation. Label the chosen controller with **Reference** for priority use.
- Install sensors for automatic target detection.
- Attach antennas for enabling network target sharing functionality.

### Custom Data Configuration
Customize radar functionality directly in the programmable block's Custom Data. Changes will take effect within 10 seconds of saving.

## Multiscreen Display
To create a multiscreen radar display:
1. Arrange multiple LCD panels into a grid.
2. Name the top left panel **Radar**.
3. Add the following to the Custom Data of that panel:
[Radar - Multiscreen Config] Screen rows=2 Screen cols=2
4. Adjust the rows and columns as needed.
5. Run the argument **refresh** to apply.

## FAQ

### General Questions
- **Will this script work with sensors?**
Yes, simply add sensors to your ship for target detection.

- **How is the radar range determined?**
By default, the radar uses the maximum range of your turrets, but this can be overridden.

- **How do I detect enemies and neutrals?**
Utilize your ship's turrets to detect targets.

- **Can I filter radar displays?**
Yes, use the **threat** argument to customize what is displayed based on threat levels.

### Technical Questions
- **Does this script work with modded turrets?**
Yes, it supports most modded and longer-range turrets.

- **What about compatibility with other radar scripts?**
This script is designed to integrate smoothly with existing systems, including configurable IFF messages.

### Author's Notes
I hope you enjoy using the Enhanced Turret-Based Radar System! Please report any bugs or suggestions in the Bug Reports discussion. Your feedback is crucial for ongoing improvements!
