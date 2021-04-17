# FRANKA DOCKER INSTALALTION

FROM ros_base:latest


# LIBFRANKA INSTALLATION

RUN apt upgrade && apt install -y build-essential \
                   apt install -y cmake \
                   apt install -y git \
                   apt install -y libpoco-dev \
                   apt install -y libeigen3-dev
# Libfranka clone
RUN git clone --recursive https://github.com/frankaemika/libfranka \
    cd libfranka

# Librfranka build
RUN mkdir build \
    cd build    \
    cmake -DCMAKE_BUILD_TYPE=Release .. \
    cmake --build .
