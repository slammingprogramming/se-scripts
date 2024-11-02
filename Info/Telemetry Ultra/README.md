# Telemetry Ultra

## Description
Welcome to Telemetry Ultra! This enhanced script takes ship telemetry tracking to the next level. It consolidates all your ships' telemetry data into a single, intuitive interface, allowing for effortless monitoring and management of your fleet.

With Telemetry Ultra, you’ll enjoy a Radar-like visual display for real-time tracking of ship locations, instantly identifying any ships with damage, core problems, or those that are 'missing' using color-coded alerts. This script builds upon the foundation of the popular Telemetry script originally authored by Magistrator, with a host of new features and enhancements designed to improve your experience.

> **Note**: For a comprehensive overview of all features, refer to the FULL GUIDE.

## Features
- **Comprehensive Ship Monitoring**: View telemetry data for all your ships on one or more screens.
- **Visual Telemetry Display**: A radar-like visual representation of ship locations for enhanced situational awareness.
- **Color-coded Alerts**: Instantly recognize ships with damage, core issues, or those marked as missing.
- **Enhanced Telemetry Data**:
  - Ship name
  - Status (if not normal)
  - Velocity and altitude
  - Battery, hydrogen, and oxygen levels
  - Damage level and cargo capacity
  - Docked grid status
  - GPS location and last update
  - Shield percentage (for Shield Defense MOD)
- **Alerts Dashboard**: Simplified reading of each ship's status and GPS location with automatic scrolling.
- **LCD Font Customization**: Adjust the font size on the alert display for better readability.
- **Custom Data Settings**: Easily configure telemetry settings to suit your needs.
- **GPS Data Options**: Show GPS data rounded to 4 decimal digits by default or in 'long' format with higher accuracy.
- **Separate LCD for GPS Data**: Functionality for a separate LCD screen to show GPS data using the tag `[TelemetryGPS]`.
- **Ship Aliases**: Create aliases for ships shown in any given collector by adding `[TelemetryPlusAliases]` to the Custom Data of the PB.
- **Reporting Interval**: Configure the reporting interval (default=5 seconds) for broadcasting ship locations.
- **Max Antenna Range**: (default=50000) Limit the broadcast range when identifying 'hiding' ships.
- **Multiple PB Support**: Allows for multiple PBs on the same grid for larger applications.
- **Damage Reporting Fix**: Improved handling of damage reporting for docked ships.
- **Improved Readability**: Added a dashed line separator between telemetry data packets for easier reading.

## Setup Instructions

### Required Steps
1. Subscribe to this script on the Steam Workshop.
2. Place a Programming Block (PB) on your ship and load this code (click Edit, then Browse Scripts, and select Telemetry Ultra).
   - **Note**: Ensure your ship is not connected to a base when installing the code for accurate damage reporting.
3. Place a PB in your base and load the script using the same process.
4. Configure Custom Data in the base PB:
   - Set `collector` to `true`.
   - Add the TAG `[Telemetry]` to the name of a text panel (usually an LCD) in your base (e.g., "LCD [Telemetry]").
   - Add the TAG `[VTelemetry]` to a text panel or console block in your base.
   - Add the TAG `[TelemetryAlert]` to a text panel/LCD in your base to see only ships broadcasting 'alert' status.
   - Set up ship aliases using `[TelemetryPlusAliases]` in the Custom Data of the PB.

## Settings
Customize the following in the Custom Data of the Programming Block:
- `collector`: Set to true to enable this PB as a telemetry collection node.
- `panel_tag`: Text panels with this `[tag]` will display the telemetry.
- `visual_tag`: Text panels or console blocks (projector) with this `[tag]` will display visual telemetry.
- `alert_panel_tag`: Text panels with this `[tag]` will display ALERT telemetry.
- `subgrid_panels`: Set to true to enable this PB to write to panels in other subgrids.
- `security_key`: Change this to prevent other factions from seeing your telemetry.
- `channel`: Assign ships to different channels for telemetry broadcasts.

## Commands
Run these commands as arguments in the Programming Block:
1. Select the PB (Programming Block).
2. Scroll down to the Argument area and enter the desired command.
3. Click Run.

| Command                | Description                                                      |
|-----------------------|------------------------------------------------------------------|
| `scale`               | Changes the visual telemetry scale (20m, 200m, 2km, etc.).      |
| `save`                | Saves telemetry data to PB Storage.                              |
| `clear`               | Clears telemetry data.                                           |
| `orbit <altitude>`    | Calculates the exact orbit position above the current location at the given altitude in meters and adds the GPS entry to the Custom Data. Example: `orbit 42000`. |

## Important Notes
- This script replaces the original Telemetry & Telemetry Plus script by Magistrator and TechCoder, respectively. Ensure all bases and ships are updated to utilize the full range of features.
- Be sure to rate and favorite this script to support continued development!

Thank you for using Telemetry Ultra! Your support means a lot, and I hope you enjoy enhanced telemetry tracking in your Space Engineers adventures!
