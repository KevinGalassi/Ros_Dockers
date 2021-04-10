# UR DOCKER INSTALALTION

FROM ros_base:latest



# For Find_Object_2d taht require Q4.x versio
RUN apt install -y qt4-default

# UR library required
RUN apt install -y ros-melodic-ur-client-library

                  
# FCL installation required for Collision checker
RUN git clone https://github.com/flexible-collision-library/fcl \
    cd fcl \
    mkdir build && cd build \\
    cmake .. \
    make install

