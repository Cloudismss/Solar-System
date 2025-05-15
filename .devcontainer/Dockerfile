# Arch Linux base development package
FROM archlinux:base-devel

# Update distro and install C++ packages
RUN pacman -Syu  --noconfirm \
    git \
    gdb \
    gcc \
    clang \
    lldb \
    lldb-mi \
    ninja \
    cmake \
    cppcheck \
    valgrind \
    doxygen \
    bat \
    && pacman -Scc --noconfirm

# Install raylib dependencies
RUN sudo pacman -S --noconfirm \
    alsa-lib \
    mesa \
    libx11 \
    libxrandr \
    libxi \
    libxcursor \
    libxinerama \
    && pacman -Scc --noconfirm

# Copy local directory to docker container
COPY .. ./Solar-System

# Set docker container working directory
WORKDIR /Solar-System
