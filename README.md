# ws_livox usage

1. Install the ROS dektop full:
    ```bash
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
    sudo apt update
    sudo apt install ros-noetic-desktop-full
    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    ```

2. Install libraries:
    ```bash
    sudo apt install ros-noetic-gps-common
    sudo apt install ros-noetic-swri-math-util
    sudo apt install ros-noetic-swri-roscpp
    sudo apt install ros-noetic-swri-serial-util
    sudo apt install ros-noetic-swri-string-util
    sudo apt install ros-noetic-swri-nodelet 
    sudo apt install libpcap-dev
    ```

3. Enable serial port:
    ```bash
    sudo usermod -a -G dialout $USER
    ```

4. Install the livox node:
    ```bash
    git clone https://github.com/liang-tang/ws_livox/
    ```

5. Compile:
    ```bash
    cd ws_livox
    catkin_make
    ```

6. Environment setup:
    ```bash
    echo "source  ~/ws_livox/devel/setup.sh" >> ~/.bashrc
    source ~/.bashrc
    ```

Welcome to join us.
QQ group: 1033644961
