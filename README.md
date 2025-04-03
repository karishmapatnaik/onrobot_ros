# 🤖 OnRobot Gripper Control (ROS 2)

This **ROS 2 package** provides a lightweight interface to control an **OnRobot gripper** via a simple ROS 2 node. The node subscribes to a topic and interprets string commands to open or close the gripper.

---

## ✨ Features

- ROS 2 Humble compatible
- Listens to `/gripper_command` topic
- Simple string-based control interface
- Easy integration with larger robot stacks
- Tested with OnRobot hardware

## 🔧 Test

1. Launch the gripper control node in one terminal:

   ```bash
   ros2 run onrobot_ros gripper_control

2. In a new terminal, source your ROS 2 Humble setup and workspace overlay: `source /opt/ros/humble/setup.bash` `source ~/your_ws/install/setup.bash`

3. Send a command to the gripper:

    To close the gripper:
   ```bash
   ros2 topic pub --once /gripper_command std_msgs/String "{data: 'close'}"
   ```
    To open the gripper:
   ```bash
   ros2 topic pub --once /gripper_command std_msgs/String "{data: 'open'}"
   ```
    To set a particular width in **mm**:
   ```bash
   ros2 topic pub --once /gripper_command std_msgs/String "{data: '200'}"
   ```
