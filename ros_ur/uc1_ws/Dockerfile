# UR5 DOCKER INSTALALTION

FROM ros_ur:latest


# FCL installation required for Collision checker
# ( "sed command" remove check_required_components macro that cause  compilation error )
RUN git clone https://github.com/flexible-collision-library/fcl && \
    cd fcl && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make install && \
    sed -i '$d' /usr/local/lib/cmake/fcl/fcl-config.cmake

RUN git clone https://github.com/gadomski/cpd && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make    && \
    make install \