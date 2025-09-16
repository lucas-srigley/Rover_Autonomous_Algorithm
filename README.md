# Rover Simulation Project

A ROS-based rover simulation with obstacle avoidance using Gazebo and laser sensors.

## Features

- Obstacle detection with laser sensors (stops within 0.5m of objects)
- Configurable speed control for left/right wheels
- Real-time position tracking

## Quick Start

1. **Start simulation:**
   ```bash
   roslaunch owen_launch gazebo.launch
   ```

2. **Run rover control:**
   ```bash
   python3 code_snipets/example_alg.py    # Conservative speed (7)
   python3 code_snipets/test1.py          # High speed (14)
   ```

3. **Send destination (optional):**
   ```bash
   rostopic pub /destination sensor_msgs/NavSatFix [parameters]
   ```

## Code Structure

- `example_alg.py` - Basic obstacle avoidance algorithm
- `test1.py` - Higher speed test version
- `usefull_command_line_stuff.txt` - ROS command reference

## Dependencies

- ROS + Gazebo
- Python 3
- `qset_lib` (custom rover library)

## How It Works

The rover continuously monitors laser distance sensors and stops both wheels when any obstacle is detected within 0.5 meters. Simple but effective for basic navigation safety.
