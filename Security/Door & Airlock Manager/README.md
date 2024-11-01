# Door & Airlock Manager
**Version:** 0.0.0
**Date:** 2024-10-31  
**Author:** SlammingProgramming  

## Overview
The Door & Airlock Manager is a sophisticated automation script for Space Engineers that provides real-time control of doors and airlocks without the need for timers. This script enhances responsiveness to player movement and environmental changes, offering versatile functionality for various ship or base configurations. It supports both All-in-One (AIO) and Separated O2 systems, making it adaptable for different use cases and atmospheric conditions.

## Key Features

### Real-Time, Timer-Free Automation
- **Event-Driven Logic:** Eliminates timers, utilizing immediate sensor input to control door operations, venting cycles, and status displays.
- **Instant Response:** The system reacts in real-time to player or vehicle presence, ensuring optimal door and airlock management.

### Flexible O2 System Modes
- **All-in-One (AIO) Mode:** Utilizes interconnected conveyor systems for shared O2 tanks and air vents, facilitating centralized O2 storage and air balancing.
- **Separated O2 Mode:** Keeps airlock systems isolated, preventing air cross-flow and allowing precise control over airlock pressurization without affecting the base atmosphere.

### Advanced Automated Control Options
- **Adaptive Pressure Cycles:** Instantly adjusts pressurization based on entry/exit detection and current airlock status.
- **Automated O2 Recycling:** Prioritizes recycling O2 before external venting, minimizing waste.
- **Multi-Environment Support:** Automatically adjusts operations for vacuum, atmospheric, and pressurized conditions based on internal and external readings.

### Simplified Manual Override System
- **Single Button Overrides:** Located at key points for easy manual control of doors and airlock functions.
- **Emergency Lockdown Mode:** Seals all doors and suspends automated operations for maximum security during emergencies.

### Expanded Status Display and Notifications
- **Real-Time Indicators:** Displays airlock pressurization levels, door status, and current operation mode on multiple LCD panels.
- **Environmental Alerts:** Provides notifications for critical changes, such as transitioning to a depressurized environment or low O2 levels.

### Flexible Modular Setup
- **Adaptive Block Naming:** Supports custom naming conventions for easy integration with various setups, including multi-airlock systems.
- **Configurable Sensor Zones:** Allows for tailored detection ranges for players and larger vehicles, accommodating complex layouts.

## Installation Instructions
1. **Script Upload:** Upload the Door & Airlock Manager script to your programmable block.
2. **Basic Setup:** Ensure the game is in experimental mode and that in-game scripts are enabled in world options.
3. **Configuration:** Modify the script settings to define the names of all necessary blocks (doors, sensors, air vents, etc.) for proper functionality.

### Required Components
- **Blocks Required:**
  - **Programmable Block:** Where the script is installed.
  - **Hanger Doors:** Two doors (interior and exterior) must be named for identification.
  - **Sensors:** 
    - 1 Interior Sensor (detects entities at the interior door)
    - 1 Exterior Sensor (detects entities at the exterior door)
    - 1 Airlock Sensor (covers the airlock space)
  - **Air Vent:** Depending on the O2 system mode, either one central vent (AIO) or two (for Separated O2).
  - **O2 Tanks:** At least one tank for managing air levels.

- **Optional Components:**
  - **Control Buttons:** For manual operation at each door and a central console.
  - **LCD Panels:** For displaying status information at strategic locations.
  - **Sound Block/Light Indicators:** For additional alerts during airlock operations.

## Detailed Script Functionality

### Real-Time Door and Pressure Control
- **Automatic Door Locking Sequence:** Ensures only one door is open at a time to maintain airlock integrity. If the airlock is pressurized, the other door remains locked until the first is closed.
- **Instant Pressurization/Depressurization:** The script immediately adjusts air pressure when entities are detected.
- **Sensor-Activated Cycling:** Initiates the appropriate cycle (pressurization or depressurization) based on sensor input.

### System Mode Configuration
- **AIO Mode:** Shares O2 with the base atmosphere, using a central air vent for efficient pressure management.
- **Separated O2 Mode:** Uses isolated O2 systems for airlocks, ensuring that breaches do not affect the primary atmosphere.

### Environment-Adaptive Air Management
- **O2 Recycling Efficiency:** Prioritizes internal O2 conservation during depressurization.
- **External Condition Detection:** Automatically adjusts venting processes based on the external environment.

### Enhanced Manual Control and Emergency Overrides
- **Manual Override Mode:** Enables users to bypass automation for manual control of doors and airlock functions.
- **Emergency Mode:** Locks down all doors and suspends sensor activity in emergencies.
- **Quick Reset Function:** Returns the airlock to default automated mode from manual control.

### Expanded LCD and Alert System
- **Centralized Status Display:** Shows airlock pressure, door positions, and operation modes.
- **Visual and Audible Cues:** Optional alerts for critical operations or emergency situations.

## Customizing and Expanding the Script
- **Dynamic Naming:** Use flexible naming schemes for easy integration into various ship or base configurations.
- **Multi-Room Support:** Extend functionality to support adjacent rooms or additional docking areas.
- **External Control Integration:** Optional connections to remote controls for managing airlocks from a distance.

This fully automated, timer-free airlock control system offers real-time responsiveness, enhances O2 efficiency, and supports a wide range of configurations. The dual-mode compatibility with both AIO and separated O2 setups provides the flexibility needed for complex systems, while integrated manual and emergency controls ensure players maintain full operational command.
