# DOCKERFILE ROS-BASE INSTALLATION

FROM ros:melodic-ros-core-bionic

# install bootstrap tools
RUN apt-get update && apt-get install --no-install-recommends -y \
    build-essential \
    python-rosdep \
    python-rosinstall \
    python-vcstools \
    && rm -rf /var/lib/apt/lists/*

# bootstrap rosdep
RUN rosdep init && \
  rosdep update --rosdistro $ROS_DISTRO

# install ros packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-melodic-ros-base=1.4.1-0* \
    && rm -rf /var/lib/apt/lists/*

# Installation of EIGEN3
RUN apt update && apt install -y libeigen3-dev

# ROS Desktop packages
RUN apt install -y ros-melodic-moveit && \ 
    apt install -y ros-melodic-moveit-visual-tools

RUN apt update && apt install -y ros-melodic-ros-control && \
    apt install -y ros-melodic-ros-controllers && \
    apt install -y ros-melodic-ros-controllers && \
    apt install -y ros-melodic-geometry && \
    apt install -y ros-melodic-tf2-bullet


# Ros RQt/RViz/Gazebo packages

RUN apt update && apt install -y ros-melodic-rqt && \
    apt install -y ros-melodic-viz && \
    apt install -y ros-melodic-gazebo-ros-pkgs && \
    apt install -y ros-melodic-gazebo-ros-control