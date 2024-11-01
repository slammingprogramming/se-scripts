# Docked Ship Info

## Description
**Docked Ship Info** is an advanced script designed to seamlessly monitor and display real-time information about all currently docked ships within your hangars. This feature-rich tool provides detailed statistics, ensuring you stay informed about the status of your vessels at all times. Perfect for any space engineer, this script enhances your gameplay by facilitating efficient management of your docked ships.

### Current Version:
- **Version:** 0.0.0
- **Release Date:** 10/31/2024

## Core Features
- **Dynamic Ship Tracking:** Automatically detects and displays names of all currently docked ships.
- **Connector Monitoring:** Identifies which connectors ships are docked to, ensuring smooth operations.
- **Comprehensive Ship Statistics:** Offers a detailed overview of vital ship metrics, including battery, hydrogen, oxygen, and cargo levels.
- **Highly Customizable LCD Content:** Adjust the display settings via custom data settings for a tailored user experience.
- **Scrolling Text Display:** Automatically scrolls long lists on LCD panels, ensuring no information gets cut off.

## Enhanced Features
### Real-Time Automation
- **Instant Updates:** The script responds instantly to changes in docking status, providing up-to-the-second information on docked ships.
- **Environmental Awareness:** Automatically adjusts displayed information based on ship conditions (e.g., atmospheric changes, power levels).

### User-Friendly Interface
- **Master Options Configuration:** Set default values for all LCDs using master options within the script config, which apply to newly added LCDs.
- **LCD Customization:** Enable or disable features such as:
  - Ship health indicators
  - Battery charge levels
  - Oxygen and hydrogen metrics
  - Cargo space availability
  - Connector names and docking times

### Visual Enhancements
- **Adaptive Display Settings:** Customize your LCD's appearance with visual options for better readability and aesthetics, including sorting, spacing, and the option to show free connectors.
- **Grouped Connector Monitoring:** Monitor specific connectors or groups for optimized output, ideal for large hangars or complex docking systems.

## Setup Instructions
### Basic Setup
1. **Create an LCD Panel:**
   - Name it `IDS-main` to act as the primary display.
2. **Configure a Programmable Block:**
   - Install the script into the programmable block, check the code, then save and exit.
3. **No Timer Required:** Enjoy a smooth operation without the hassle of timer settings.

### LCD Options
Customize your LCD settings via custom data by defining the following keys:
- **Master Options:**
  useMasterOptions=true
#### Basic Settings:

showNumbers=true
showDockingTime=true
showConnectorName=true
showShipHealth=true
showBatteryCharge=true
showHydrogenLevel=true
showOxygenLevel=true
showCargoLevel=true

#### Visual Settings:

showHeading=true
compactShipStats=false
scrollText=true
showFreeConnectors=true
sortByConnector=true
emptyLineBetweenEntries=true

#### Monitored Connectors

Monitor specific connectors or groups for improved clarity. Leave blank to monitor all:
monitoredConnectors=
showGroupHeading=true

### LCD Panel Setup

####Using LCD Panels
To utilize the LCD panels effectively, include specific keywords in their names, which will be converted to the universal [DockedShipInfo] keyword.

#### LCD Keywords
- **Main LCD:** Displays all docked ships.
  - **Keyword:** `IDS-main`
- **Warning LCD:** Dedicated screen for alerts and issues.
  - **Keyword:** `IDS-warnings`
- **Performance LCD:** Displays script performance data.
  - **Keyword:** `IDS-performance`

#### Multi-Panel Screens
To spread the display across multiple screens, assign the same group tag:
1. Use the keyword IDS-main for each screen.
2. In the custom data, set the first line as follows:

@0 IDS-main:GROUP#

### Important Notes
Ownership Verification: Ensure that all blocks used are owned by you (Owner: Me).

### Known Bugs / Planned Features

Currently, there are no known bugs. Future enhancements are in consideration.

---
Enjoy managing your docked ships with Docked Ship Info!