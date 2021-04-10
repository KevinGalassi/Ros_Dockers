# Ros_Dockers
My very simple collection of Docker's images for my ROS packages. <br>
The first image to build is "ros_base" which contains a common initial image over which a new more specific image can be created, this initial image contain a ros-base installation and other basic package ( rviz, rqt, gazebo, control/controllers, moveit ...) <br>
The other images contain specific installation for the usage of a UR Robot or a Franka.
