# Power and H2 Manager
**Version:** 0.0.0
**Author:** SlammingProgramming  
**Last Updated:** 10/31/2024  

## Overview
The Power and H2 Manager is a highly configurable energy management tool designed for a variety of craft types, including ships, rovers, stations, and more. This versatile script automates power and hydrogen usage monitoring, ensuring optimal resource management across all your creations. Seamlessly integrating with other scripts, it provides comprehensive functionality for any craft you can imagine.

## Key Features

### Versatile Craft Management
- **Universal Compatibility:** Works with ships, rovers, stations, and any craft configuration you design.
- **Highly Configurable:** Tailor the script’s behavior to suit your specific craft's needs, from energy management to resource storage.

### Power Monitoring & Management
- **Current Power Output:** Displays the average output of all reactors and solar panels, helping you optimize power generation.
- **Battery Status Monitoring:** Tracks charge levels of discharging and recharging batteries to keep you informed about your energy reserves.
- **Power Usage Analysis:** Provides insights into the average power usage of solar panels, reactors, hydrogen engines, etc. relative to their maximum capacity.

### Hydrogen and Oxygen Monitoring & Management
- **Hydrogen Level Tracking:** Monitors hydrogen levels in tanks, alerting you when supplies are low or refueling is needed.
- **Oxygen Tank Management:** Automatically manages oxygen tanks as configured even when docked, ensuring resource optimization.
- **Refueling System Integration:** Automatically initiates refueling processes when hydrogen levels drop below a predefined threshold.

### Solar Panel Alignment and Management
- **Dynamic Alignment:** Automatically adjusts solar panels on rotors or gyroscopes for maximum efficiency, supporting both T-shaped and U-shaped solar arrays.
- **Multiple Tower Support:** Manage multiple solar towers simultaneously from a single programmable block.
- **Night Mode:** Stops all rotor operations until sunlight is detected again, optimizing energy use during non-productive hours.
- **Sunrise Position Reset:** Automatically rotates solar panels back to the sunrise position during the night.

### Automatic Docking Management
- **Automatic Battery Management:** Sets batteries to recharge when connected to a station and reverts them to normal when disconnected.
- **Automatic Tank Management:** Switches hydrogen and oxygen tanks to stockpile mode upon docking.

### Light Control
- **Automatic Light Adjustment:** Controls your ship's lights based on current light levels, measured with solar panels, to optimize visibility and energy use.
- **Base Light Management:** Optionally manages base lights and spotlights based on location time calculations, enhancing visibility during the day.

### Emergency Features
- **Emergency Reactor Management:** Activates reactors as a fallback if battery levels drop critically or if batteries become overloaded, ensuring continuous power supply.
- **Dynamic Notifications:** Provides real-time updates on system operations and statistics via LCD panels or text displays.

### LCD Display Integration
- **Customizable Displays:** Utilize LCDs tagged with the LCD_DISPLAY_TAG to show detailed craft-wide power and hydrogen breakdowns. Customize colors and font sizes through variables like LCD_DISPLAY_COLOUR, LCD_DISPLAY_FONT_COL, and LCD_FONT_SIZE.
- **Status Updates:** Displays information about the current system status in the programmable block, LCDs, or text panels, along with statistics in block names.

### Prefix Filtering for Craft-Specific Control
- **Prefix Support:** Enable prefix filtering by setting the SHIP_PREFIX variable to limit script actions to blocks that start with a specific string, preventing interference with docked ships.

### Solar Position Calculation
- **Solar Positioning:** Calculates the optimal angle and orientation of solar panels based on real-time solar position, maximizing energy capture.

### Additional Ideas for Future Features
- **Resource Consumption Analytics:** Provide detailed analytics on resource consumption trends for better long-term planning.
- **Custom Alert System:** Allow users to define custom alert conditions for various events, such as low power, low hydrogen, or critical battery levels.
- **User Interface Enhancements:** Develop a user-friendly GUI for managing settings without needing to edit code directly.
- **Enhanced Support for Multiple Craft Types:** Further customization options for different types of craft configurations, optimizing performance based on specific use cases.

## Installation Instructions
1. **Script Upload:** Upload the Power and H2 Manager script to your craft’s programmable block.
2. **Display Setup:** Ensure you have one or more LCDs tagged with the Display keyword for data output.
3. **Tag Configuration:** Adjust the names of text panels or blocks to include relevant tags for proper function.
4. **Basic Setup:** No timers are required! Just set up the programmable block with the script, check the code, and you’re done.

### Optional Settings:
- Modify the SHIP_PREFIX variable to filter which blocks the script interacts with.
- Configure sound and light tags for alerts and visual indicators.

## Customization
Customize the Power and H2 Manager’s appearance and functionality through the Custom Data of the programmable block. Simply modify the settings and click "OK" to apply your changes instantly.

### Color Customization
Easily change the colors and font sizes in the programmable block's custom data to suit your preferences.

## Frequently Asked Questions
- **Can I customize the color of the displays?**
  Yes, colors can be modified in the custom data of the programmable block.

- **Is the Power and H2 Manager compatible with other scripts?**
  Absolutely! This script integrates seamlessly with other scripts for enhanced functionality across your craft.

- **How do I set power alarm thresholds?**
  Adjust the LOWPOWER variable to set your desired power alarm threshold.

- **How does the solar position calculation work?**
  The script calculates the optimal angle for solar panels based on the current solar position, enhancing energy capture.

- **How does the hydrogen and oxygen management work?**
  The script automatically adjusts battery settings upon docking, switches hydrogen and oxygen tanks to stockpile mode, and provides alerts for low hydrogen levels.

## Bug Reports & Feedback
Please report any bugs or share your feedback in the dedicated discussion area. Your contributions are invaluable for enhancing the Power and H2 Manager experience!