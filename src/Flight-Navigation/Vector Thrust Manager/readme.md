# Vector Thrust OS
### Fork from VectorThrust2
### Self rotating thrusters.

### Big thanks to Digi, Whiplash, d1ag0n, feoranis, Malware, and so on to help me with part of the code and solving some problems.
### I cannot rule out my thanks also to 1wsx10, the original author of Vector Thrust 2 and for providing the mayority of the code where this script is working.

Workshop link: https://steamcommunity.com/sharedfiles/filedetails/?id=2831096030

Mod.io link: https://spaceengineers.mod.io/vector-thrust-os

## What's new:
- The movement now is really smooth and clean in the mayority of times.
- Improved performance considerably.
- Fixed the vibrations that do the rotor thrusters in space and in planets, using a trained AI to determine how much aggresive has to act the rotors.
- Added the Role and Grouping of rotor thrusters to improve coordination.
- There is no longer standby mode, the script can handle when it's parked and shut down everything to not affect performance.
- There is no longer jetpack mode, the script have it's own acceleration system, if you assign values less than 0 it will be more confortable to toggle.
- All configuration that can be modified to improve something is written and read by the Custom Data of the Programmable Block where the script is running.
- Tag assignation is fully customizable and now easy to implement.
- You can park with landing gears and connectors and assign which batteries and tanks will be set to recharge/stockpile.
- Fixed the bug where the dampeners goes crazy.
- Fixed the bug where for some reason you were able to control other vector thrusters remotely, causing many clang accidents.
- Implemented a better method to shut down thrusters while braking/cruise mode.
- Improved UI.
- Added some utilities to handle configuration, like Runtime Tracker by Whiplash or SimpleTimerSM by Digi.
- And the list goes on...

## BASIC SETUP
1. Add a controller, and the programmable block, I recommend building everything in the same grid as the programmable block.

2. Add all the vector thrusters (recommended same grid), it can be hinges or rotors (rotors recommended), you can't stack any other vector thrust on the default one, it will get ignored. 

2,1. (OPTIONAL) Add multiple vector thrusters in the same axis, but BE CAREFUL, you have to build the strongest one in the center of mass (To get center of mass go to your Inventory, click "Info" tab then check "Show Center of Mass").

3. Download the script on mod.io or Steam Workshop, search the script and load it into the programmable block (Click Edit), then click 'Save & Exit', no need to modify any variables in the script, all configuration is on Custom Data.

4. Setup your buttons.. either use 'Control Module' by DIGI or add the option "Run" on the programmable block with the basic arguments (gear, cruise, dampeners).

## RECOMMENDED SETUP
1. Same as BASIC SETUP.

2. Same as BASIC SETUP, but you can discard one vector thrust with a specific axis direction and add normal thrusters instead.

2-1. Same as BASIC SETUP.

3. Add Vanilla thrusters (I mean the normal ones) to the grid, 1 in each direction (minimum one), with this you don't need to add the argument "dampeners" anymore, and gains better stability (if for some reason it's not stable).

4. Add a Landing Gear and/or a Connector.

5. Try driving your ship, if is really light or heavy and you seem to have movement problems, Go to the CustomData if the Programmable Block and reduce (if it's light) or increase (if it's heavy) the "Rotor Stabilization Multiplier=" value (Vector Thruster Stabilization Category).

6. Go to CustomData, setup your tag name (Main Category: NameTag=) and tag surround (OPTIONAL) (MISC Category: Tag Surround Char(s)=), tag surround can be 1 character or various characters in pairs (Example: |, or [], or (), or [[]]).

7. Wait for the (Refreshing at X s) to be zero (In the programmable block output) or press "Recompile" to apply all settings.

8. Disconnect from any external grid and run only 1 time the argument "applytags" on the programamble block, it will tag everything and it will ignore every other block from now on.

9. (OPTIONAL) Add the same tag appendix that has your programmable block to your battery, gas tanks and connector and landing gear to handle parking and best performance.

10. If you are using a cockpit as controller add your name tag followed by a colon and the number of screen (first screen starts at 0 and so on), for example, if you have as name tag "VT" and your desired screen is the left up one, you should write "VT:1". (You can see an example in the last line of the Custom Data of the PB).

11. (Optional) Customize your acceleration values, go to Custom Data Acceleration Settings Category, each value is separated by a comma, you can't put less than 2 values. To get the maximum propulsion possible of your vector thrusters I recommend to be the minimum value to -2 and maximum around 4, everything further than that may be useless and may cause problems, it depends on the thruster.

12. Add in you actions menu of the ship the action "Run" of the current programmable block and for each slot add the "gear" and "cruise" as arguments, if you don't have any normal thrusters then you can toggle dampeners with argument "dampeners".


## ADVANCED SETUP
1. Follow steps 1 to 7 of Recommended Setup.

2. Do the same as step 8, but instead of the argument "applytags", do "applytagsall" instead, that will register every block that needs the script to work (Landing gear, Connectors, Tanks, Batteries).

3. Add a small battery and DO NOT add the Tag in its name. (This is because the rest of the batteries will be set to recharge when you park with connector and leave 1 as the backup battery).

4. Follow steps 9 - 12, but in step 11 add all the thrusters connected at your rotors/hinges in the action bar as "Increase Thrust Override", add the argument "gear" of the PB too then toggle to the max acceleration and move forward, if you see that one or more thrusters in the action bar doesn't display 100% of its thrust override increase the last acceleration in the Custom Data configuration. Then you can set the default acceleration that will assign the script on reload (Starting Acceleration Position=), being 0 the first and so on.

5. If the grid is going to work in space, you have to take in count if the vector thrusters do a shake or vibration when it tries to reposition them to reach 0 m/s, so you can fix that enabling (In Vector Thruster Stabilization Category) "Slow Reposition Of Rotors On Turn Off=" and setting your maximum custom RPM at "Slow Rotor Reposition Value (RPM)=" to any value you want (Maximum 60, I prefer leaving it at default).

6. Finally Recompile the script one more time and increase the "Time For Each Refresh=" to 999 to evade these problems, also the "Time Checking Intervals=" to a higher number than 1 (It handles the new screens added and block check).
### IMPORTANT, IF YOU FEEL THAT THE THRUSTERS FEEL STRANGE, INCREASE ROTOR TORQUE AND BRAKING TORQUE


## SCRIPT IS HEAVY FOR YOUR SERVER?

Don't worry! There's an option I added for that desired low end gameplay, I present you "Skipframes=", each frame is processed, N frames will be skipped, improving performance but making the script less precise the more the value, I recommend putting it no more than 4 in space and 2 in planets. 
Example: Assuming if the frame that will not be processed is [0] and processed [1]. If you set Skipframes to 1, the frames will go like this: [0][1][0][1]...
But if you set it to 3, it will go like this: [0][0][0][1][0][0][0][1]

## VANILLA BUTTONS SETUP
1. Get in your Controller (Cockpit, Remote Control), press G.
2. Drag the Programmable Block to the bar and select "Run".
3. Write or paste the argument for your controls. you will need:
* gear
* cruise
* dampeners (If you don't have any normal thrusters avaible, otherwise use vanilla [Z]).

## CONTROL MODULE SETUP (Probably Deprecated)
Install the Mod and you're good to go!
### BUTTONS 
* __inertia dampeners key__:	Inertia Dampeners On/Off.
* __boost key__: Increase acceleration by a value while holding.
* __decrease boost key__: Decrease acceleration by a value while holding.

## INFO PANEL SETUP
#### While this is Optional, I highly recommend it.
1. Place a text panel
2. put *__NameTag__LCD in the name
3. For Controller screens add *__NameTag__:n , where n can be from 0 to the (length of all screens available - 1).

## BUGS
Sometimes if the thruster is so strong, at full acceleration, the vector thruster that doesn't have to do anything does a really zigzag pattern, it doesn't affect gameplay.
If you want to report a bug go to Issues tab.
