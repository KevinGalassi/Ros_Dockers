# UR5 DOCKER INSTALALTION

FROM ros_base:latest


# For Find_Object_2d taht require Q4.x versio
RUN apt install -y qt4-default

# UR library required
RUN apt install -y ros-melodic-ur-client-library && \ 
    apt install -y ros-melodic-industrial-robot-status-interface \
    apt install -y ros-melodic-ur-msgs

# FCL installation required for Collision checker
# ( "sed command" remove check_required_components macro that cause  compilation error )
RUN git clone https://github.com/flexible-collision-library/fcl 

RUN cd fcl && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make install && \
    sed -i '$d' /usr/local/lib/cmake/fcl/fcl-config.cmake



