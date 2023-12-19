FROM ros:humble-ros-base

RUN apt-get update && apt-get install -y \
    git \
    bash-completion

RUN echo "if [ -f /etc/bash_completion ] && ! shopt -oq posix;then\n. /etc/bash_completion\nfi" >> /root/.bashrc
RUN echo ". /opt/ros/$ROS_DISTRO/setup.bash" >> /root/.bashrc

# Create ROS workspace
WORKDIR /workspace
RUN colcon build --symlink-install

