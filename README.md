# ros2_micro-ROS_DDSM115_m5StampS3
DDSM115 interface ROS2 micro-ROS on m5StampS3
- Easy to communicate m5StampS3 on usb serial without wifi, such as metalic enlosure
- Support reconnection


## Dependency
- ROS2 Humble
- micro_ros_arduino-humble

## Build and Upload
please use VS code


## Run ROS2 nodes for sending commands
### Run micro-ROS agent
```
$ ros2 run micro_ros_agent micro_ros_agent serial --dev/ttyaCM0 --baud 115200
```
### Run teleop_node

```
$ ros2 launch teleop_twist_joy teleop-launch.py joy_config:='xbox'
```
sometimes you need following command to use joystick
```
$ros2 run joy_linux joy_linux.node
```

### Useful commands for debugging
```
$ ros2 topic list
$ ros2 topic echo /joy
$ ros2 topic echo /cmd_vel
```

