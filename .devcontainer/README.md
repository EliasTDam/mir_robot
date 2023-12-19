# Devcontainer for the MiR ROS 2 driver
This container uses a ROS 2 base image (Humble), creates a ROS workspace and mounts the source code in the `src` folder.

To build from a fresh container, open a terminal and run:

    vcs import < src/ros2.repos src --recursive
    rosdep update
    rosdep install --from-paths src -i -y --rosdistro humble
    source /opt/ros/humble/setup.bash
    colcon build --symlink-install
