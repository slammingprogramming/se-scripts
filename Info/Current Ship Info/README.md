# Current Ship Info
**Version:** 0.0.0
**Date:** 10/31/2024  
**Author:** SlammingProgramming  

## Overview
The Current Ship Info script provides a comprehensive and user-friendly interface that displays essential information about your ship or station in Space Engineers. With real-time monitoring and accessibility, this script ensures you have all the critical details at your fingertips to manage your resources, power, and structural integrity effectively.

## Key Features

### Comprehensive System Monitoring
- **Battery Status:** Displays current charge levels, power consumption, and status of all ship batteries.
- **Tank Levels:** Monitors oxygen and hydrogen tank levels, ensuring you always know your fuel and life support status.
- **Cargo Container Overview:** Provides detailed information on each cargo container, including total capacity, current load, and item breakdown.
- **Air Vent Readiness:** Checks the status and efficiency of air vents to ensure adequate oxygen levels throughout your ship.
- **Reactor Performance:** Monitors the output and fuel levels of reactors, providing a clear view of your power generation status.

### User-Friendly Interface
- **LCD Display:** Easily view ship status on an LCD panel named "LCD Panel sysinfo." This name can be customized in the configuration section to fit your preferences.
- **Customizable Display Settings:** Setup the LCD with your preferred font, size, and color for optimal readability. Ensure it is set to display "Text and Images" for the best experience.

### Real-Time Updates
- **Dynamic Monitoring:** The script automatically checks for newly added or removed blocks, keeping the displayed information current as you modify your ship or station.
- **Configurable Check Interval:** The default check time is set to 15 seconds, which can be adjusted at the head of the script to suit your needs.

### Detailed Resource Management
- **Resource Summary:** Provides a clear summary of all essential resources, including batteries, tanks, cargo containers, and reactors.
- **Alerts and Notifications:** Sends alerts for low battery, low oxygen, or hydrogen levels, ensuring you're always prepared for emergencies.
- **Performance Tracking:** Keep track of energy efficiency and resource consumption to optimize ship performance.

### Additional Features
- **System Logs:** Keep a log of system changes and status updates for troubleshooting and performance analysis.
- **Customizable Alerts:** Set personalized thresholds for alerts based on your operational needs (e.g., low battery or low oxygen levels).
- **Compatibility with Other Scripts:** Designed to work seamlessly with other management scripts for enhanced functionality, allowing for comprehensive ship management.

## Installation Instructions
1. **Script Upload:** Upload the Current Ship Info script to your programmable block.
2. **Basic Setup:** Create an LCD panel named "LCD Panel sysinfo" (or your preferred name) and copy the script into the editor.
3. **Display Configuration:** Customize the LCD settings (font, size, color) and ensure it is set to display "Text and Images."

## Configuration Requirements
- Modify the name of the LCD in the configuration section if using a different name from "LCD Panel sysinfo."
- Adjust the check interval at the top of the script if you wish to change the frequency of updates.

## Known Issues
- **Block Removal Lag:** If blocks are removed or added quickly, there may be a slight delay in updating the display. Adjusting the check interval may help.
- **LCD Formatting:** Ensure that the LCD is set to display "Text and Images" to avoid formatting issues.
