# RGB Controller Script

## Overview

Welcome to the **RGB Controller Script** for Space Engineers! This script empowers players to create stunning RGB light effects on their ships and bases. With a wide array of customizable animation modes, you can bring your creations to life with vibrant colors and dynamic patterns. 

## Features

- **Fully Customizable**: Adjust light colors, animations, and parameters to suit your preferences.
- **Lightweight**: Minimal performance impact on your game.
- **Compatible**: Works seamlessly with both small and large ships.
- **Easy Setup**: Simple installation and configuration without the need for a Timer Block.

## Setup Instructions

1. **Place a Programming Block**:
   - Place a **Programming Block** in your ship.

2. **Add the Script**:
   - Copy and paste this script into the **Programming Block**.

3. **Group Your Lights**:
   - Group all your lights together and name the group as desired.
   - Add the tag `[LED: ***]` to your group name. Replace `***` with the desired mode and options (see Modes and Options below).

4. **Rescan After Changes**:
   - Whenever you modify a tag, remember to run the `"rescan"` argument to update the configuration.

## Tag Format

A LED tag is composed of two parts: the animation mode and a list of optional settings.

**Tag format**: 
[LED: Mode option1 option2 option3]

**Example tag**: 
[LED: Noise spd:0.6 scale:0.15]

Each part of the tag is separated by a space, and option names and values are separated by a colon (`:`). Invalid options will be ignored. Some options may not require a value.

## Modes and Options

### 1. Noise
The most basic animation, this creates a random pulsating sea of colors with your LEDs.

- **Options**:
  - `spd`: The animation speed of the noise.
  - `scale`: The scale of the animation. Smaller values make the blobs bigger.

### 2. Pulse
The most useful animation, the pulse animation is waves that travel through 3D space and your ship. LEDs that the waves hit are lit up, creating wave patterns on the ship.

- **Options**:
  - `spd`: The speed the waves travel at, in m/s.
  - `r`: The color of the waves (Red component).
  - `g`: The color of the waves (Green component).
  - `b`: The color of the waves (Blue component).
  - `dirX`, `dirY`, `dirZ`: Direction components of the wave travel vector.
  - `space`: The spacing between each wave, in blocks.
  - `width`: The width of each wave in blocks.
  - `falloff`: The falloff of the waves. Values of 1 or above create soft pulses, while values between 0 to 1 create sharp waves.
  - `noise`: Whether to map color to random colors or not (this option does not require a value).
  - `noisescale`: If using noise, this is the scale of the noise.
  - `noisespd`: If using noise, this is the speed of the noise animation independent of the wave speed.

### 3. Ripple
Like a ripple in a pond, spherical waves are created from a specified point in your ship. LEDs that the waves hit are lit up, creating ripple patterns on the ship.

- **Options**:
  - `spd`: The speed the waves travel at, in m/s.
  - `x`, `y`, `z`: Coordinates of the block the wave is emitted from.
  - `r`, `g`, `b`: Color of the waves (RGB components).
  - `space`: The spacing between each wave, in blocks.
  - `width`: The width of each wave in blocks.
  - `falloff`: The falloff of the waves. Values of 1 or above create soft pulses, while values between 0 to 1 create sharp waves.

### 4. Sweep
Useful for spinning lights, this works very similarly to a lighthouse. An axis of rotation and center point is specified. Spinning walls mounted on that axis will hit LEDs that light up to create sweeping patterns.

- **Options**:
  - `spd`: The speed the waves travel at, in m/s.
  - `waves`: The number of waves in this animation.
  - `r`, `g`, `b`: Color of the waves (RGB components).
  - `x`, `y`, `z`: Coordinates of the center of the sweep.
  - `dirX`, `dirY`, `dirZ`: Direction components of the axis of rotation.
  - `falloff`: The falloff of the waves. Values of 1 or above create soft pulses, while values between 0 to 1 create sharp waves.
  - `ratio`: The ratio of wave to actual space.

### 5. Random
The most basic of all animations, the random animation is basically your Christmas tree.

- **Options**:
  - `period`: How many seconds it takes for the lights to rearrange.
  - `cutoff`: For each light, this is the probability (0-1) that the light will be turned on.

### 6. Flash
Creates a flashing effect, turning lights on and off at a specified rate.

- **Options**:
  - `onTime`: Duration (in seconds) for which the lights are on.
  - `offTime`: Duration (in seconds) for which the lights are off.
  - `r`, `g`, `b`: RGB components of the flash color.

### 7. Fade
Gradually transitions lights between two colors over a specified duration.

- **Options**:
  - `duration`: Total time (in seconds) for the color transition.
  - `startR`, `startG`, `startB`: Starting RGB values.
  - `endR`, `endG`, `endB`: Ending RGB values.

### 8. Strobe
Creates a rapid flashing effect, similar to a strobe light, cycling through colors.

- **Options**:
  - `spd`: Speed of the strobe effect (flashes per second).
  - `colors`: Comma-separated list of RGB values (e.g., `255,0,0,0,255,0,0,0,255` for red, green, and blue).
  - `duration`: How long to strobe before switching colors (in seconds).

### 9. Wave
Generates a sinusoidal wave effect that moves through your lights, creating smooth transitions.

- **Options**:
  - `spd`: Speed of the wave (in m/s).
  - `amplitude`: Height of the wave (how many lights are affected).
  - `frequency`: How often the wave repeats (number of cycles per second).
  - `r`, `g`, `b`: RGB components of the wave color.

### 10. Breathing
Lights gradually fade in and out, creating a "breathing" effect.

- **Options**:
  - `inTime`: Duration (in seconds) for the lights to fade in.
  - `outTime`: Duration (in seconds) for the lights to fade out.
  - `r`, `g`, `b`: RGB components of the breathing color.

### 11. Spiral
Creates a spiral effect where lights light up in a spiraling motion around a specified center.

- **Options**:
  - `spd`: Speed of the spiral motion (in m/s).
  - `turns`: Number of turns in the spiral.
  - `radius`: Distance from the center to the lights.
  - `r`, `g`, `b`: RGB components of the spiral color.

### 12. Chaser
Creates a chasing light effect, where lights turn on sequentially to create a movement illusion.

- **Options**:
  - `spd`: Speed of the chase (lights per second).
  - `color`: RGB components of the chase color.
  - `reverse`: Whether the chase moves in reverse order (set as a flag, no value required).

### 13. Heartbeat
Simulates a heartbeat effect, where lights pulse in and out at a specified rate.

- **Options**:
  - `duration`: Duration (in seconds) for each heartbeat cycle.
  - `maxBrightness`: Maximum brightness value for the lights during the pulse.
  - `r`, `g`, `b`: RGB components of the heartbeat color.

### 14. Disco
Randomly changes colors at a specified interval to simulate a disco effect.

- **Options**:
  - `interval`: Time (in seconds) between color changes.
  - `minBright`: Minimum brightness level for the lights.
  - `maxBright`: Maximum brightness level for the lights.

## Troubleshooting

If you encounter any issues, please check the following:

- Ensure the script is properly pasted into the Programming Block.
- Double-check your LED tags for proper formatting.

## Contribution

If you have suggestions or enhancements for this script, please feel free to contribute! Open an issue or submit a pull request.

## Contact

For questions or support, please reach out to SlammingProgramming on GitHub.

---

Bring your ships to life with dynamic RGB lighting and enjoy your time in Space Engineers!