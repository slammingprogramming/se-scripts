# Inventory & Production Manager
**Version:** 0.0.0
**Date:** 10/31/2024  
**Author:** SlammingProgramming  

## Overview
The Inventory & Production Manager is an advanced inventory management tool designed to optimize the sorting and production processes within your Space Engineers game. This script efficiently organizes items into type-specific cargo containers while automating production, refining, and disassembly processes to ensure maximum efficiency across all operations. It also features a real-time monitoring system for cargo volume, helping you manage inventory without constant manual checks.

## Key Features

### Inventory Management
- **Cargo Container Sorting:** Automatically sorts items into cargo containers based on item type, ensuring efficient organization.
- **Internal Sorting:** Sorts items within inventories by name, amount, or type, allowing for quick access to necessary resources.
- **Container Priority System:** Assigns priority levels to containers, ensuring that the most important items are stored in the desired locations first.
- **Automatic Container Assignment:** Automatically assigns new containers if a container type is full, preventing resource overflow.
- **Special Loadout Containers:** Create designated containers with a user-defined amount of items for specific tasks or missions.

### Production Automation
- **Bottle Refilling:** Automatically refills oxygen and hydrogen bottles before storage, ensuring you’re always prepared for your adventures.
- **Auto Crafting:** Automatically produces adjustable amounts of specified items, streamlining the manufacturing process.
- **Auto Disassembling:** Automatically disassembles components when above a user-defined threshold, freeing up space and resources.
- **Assembler Cleanup:** Cleans assemblers if they become too full, ensuring continuous production flow.

### Disassembly Management
- **Disassembler Control:** Automatically turns disassemblers on and off based on demand and material availability.
- **Material Distribution:** Distributes materials equally across all disassemblers to minimize recycling time, ensuring efficient processing.
- **Component Recycling:** Pulls all components, ammo, and tools from assigned storage containers for recycling.
- **Recycled Material Management:** Returns recycled ingots back into the storage containers that originally held the materials after processing.

### Cooperative Management
- **Idle Management:** Automatically switches idle assemblers, refineries, and arc furnaces off to save energy.
- **Production Activation:** Turns production blocks on automatically when items are queued for processing, improving workflow efficiency.
- **Equal Ore Distribution:** Distributes ores equally across all refineries to ensure they work consistently over time.
- **Arc Furnace Management:** Distributes iron, nickel, cobalt, and scrap metal evenly over arc furnaces and idle refineries producing "AF ores."
- **Idle Ore Redistribution:** Redistributes ores whenever a refinery is idle, preventing resource waste.
- **Excess Ingots Drainage:** Drains excessive ingots from idle assemblers to optimize storage and prevent overflow.
- **Ingot Dumping:** Dumps produced ingots from refineries to designated cargo storage periodically, keeping inventory organized.

### Resource Optimization
- **Ore Balance System:** Automatically balances and refines the most needed ores and ingots, maximizing refinery output.
- **Ice Balance Management:** Manages ice levels for oxygen generators, ensuring a steady supply of oxygen.
- **Uranium Balance for Reactors:** Automatically manages uranium supply for reactors to maintain optimal power production.

### Cargo Volume Monitoring
- **Real-Time Cargo Volume Check:** Monitors the current volume of all cargo containers, connectors, and drills.
- **Visual Alerts:** Changes the color of a spotlight based on cargo volume limits set by the user, providing a clear visual indication of capacity.
  - **Warning Indicator:** Changes color to alert when the cargo volume reaches a specified limit.
  - **Full Indicator:** Changes color a second time when the maximum volume of the ship is reached, preventing overloading without manual inventory checks.

### User Feedback and Information Display
- **LCD Output:** Displays cargo container information and current actions on LCD panels for real-time monitoring.
- **Inventory Item Count on LCDs:** Outputs the amounts of stored items on LCD panels for easy visibility of resource availability.

### Mod Support
- **Support for Modded Items:** Fully supports modded items for autocrafting, ore balancing, and custom container loadouts, enhancing gameplay versatility.

## Installation Instructions
1. **Script Upload:** Upload the Inventory & Production Manager script to your craft’s programmable block.
2. **Basic Setup:** No timers are required! Simply check the code, remember, exit, and you're done.
3. **Experimental Mode:** Ensure your game is set to experimental mode and that in-game scripts are enabled in world options.

## Configuration Requirements
- Ensure that production blocks (assemblers, refineries, and disassemblers) have specific naming conventions:
  - Main assembler: **"Assembler MAIN [Co-op]"**
  - At least one refinery must be named **"Refinery MAIN [Co-op]"** (the main distributor).
  - Disassemblers must contain **"[CDA]"** in their names and be in disassemble mode.
  - Arc furnaces must contain **"Arc furnace"** & **"[Co-op]"** in their name to be recognized.
  - For large refineries, use **"Large Refinery"** & **"[Co-op]"** in their names.
  - Assigned storage containers must also contain **"[CDA]"** in their names and be connected to assemblers through the conveyor system.
- Set up an action for the button to run the program with the argument: **("init")**.

## Known Issues
- **Bottle Cycling:** Bottles may cycle between the O2/H2 generator and the bottle container due to game mechanics. To resolve, disable "Use Conveyor" for all generators and allow IIM to manage ice and bottle handling.
- **Container Desync:** If you encounter issues with item retrieval on dedicated servers, disable "Internal Sorting" in the script's config and relog.
- **Compatibility Issues with Mods:** Some mods may interfere with the ore balancing system. Adding "!manual" to the name of incompatible refineries will exclude them from balancing, maintaining script functionality.
