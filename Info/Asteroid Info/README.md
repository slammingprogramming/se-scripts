# Asteroid Info
**Version:** 0.0.0  
**Date:** 11/01/2024  
**Author:** SlammingProgramming  

## Overview
The Asteroid Info script is a comprehensive tool designed to enhance asteroid exploration in Space Engineers. This script not only automates the naming and accounting of scanned asteroids but also improves upon previous versions with a more user-friendly interface, advanced features, and enhanced data management capabilities.

## Key Features

### Advanced Asteroid Scanning and Management
- **Automatic Naming:** Each scanned asteroid is automatically named and stored in a database for easy identification.
- **Database Management:** Maintains a persistent database of scanned asteroids, allowing for seamless tracking and retrieval of information.
- **Search Functionality:** Implemented robust search capabilities to quickly find specific asteroids or locations.

### Enhanced User Interface
- **LCD Display:** Supports multiple Text Panels for displaying asteroid information and managing the database. Use custom keys like `_Astro0`, `_Astro1`, `_FindAstro2`, etc., to select specific LCDs for displaying data.
- **User-Friendly Commands:** Intuitive command structure with shortcuts for ease of use:
  - `Scan` - `#`
  - `Find` - `?`
  - `Note` - `n`
  - `Note+` - `n+`
  
### Comprehensive Command Suite
- **Scanning Commands:**
  - `Scan`: Scans the area in front of the ship for asteroids.
  - `Note [AnyText]`: Assigns a description to the currently selected asteroid.
  - `Note+ [AnyTextToAdd]`: Adds additional information to the current asteroid's note.
  - `Find [AnyTextToSearch]`: Searches for asteroids matching the given text.
  - `ResetBase`: Clears the current asteroid database.
  - `Update`: Refreshes the database if manual changes have been made.

- **GPS Functionality:** Users can add or remove GPS points easily:
  - `+[GPS:..]`: Adds a new GPS point.
  - `-[Name]`: Removes an existing point, case sensitive.
  - `=[Name]`: Adds the current position to a named point; generates a name if none is provided.

### Autopilot Integration
- **Remote Control Support:** Move to an active GPS point using remote control features, facilitating exploration.
- **Nearest Point Navigation:** Simply type `>SomePoint` to navigate to the nearest GPS point automatically.

### Replication and Security
- **Radio Key Security:** Use a RadioKey as a security token for safe replication.
- **Replication Control:** Set `RadioReplication` parameter to false to disable replication; default interval is set to 15 seconds for automatic updates.

### Additional Enhancements
- **Timestamped Notes:** Notes now include timestamps, replacing old entries automatically.
- **Intergrid Communication System:** Added automatic database replication between static grids, ensuring data is consistently updated.
- **Improved Error Handling:** Fixed several bugs from previous versions to ensure a smoother user experience.

## Installation Instructions
1. **Script Upload:** Upload the Asteroid Info script to your programmable block.
2. **Hardware Setup:** Ensure you have at least one Camera block, one Grid Control block, and one Remote Control for Autopilot functionality.
3. **Text Panel Configuration:** Create one or more Text Panels for displaying information and managing the database.
4. **LCD Keys Setup:** Use the provided LCD keys (_Astro, _FindAstro) to configure the Text Panels according to your preferences.

## Configuration Requirements
- Modify the LCD key names in the configuration section if you prefer different identifiers.
- Ensure your programmable block and remote control are properly set up to communicate with the required components.

## Known Issues
- **GPS Point Duplication:** Be cautious when adding GPS points; the same name may cause overwrites without warning.
