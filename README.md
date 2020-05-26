# ws_livox usage

1. Install the ROS dektop full:
    ```bash
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
    sudo apt update
    sudo apt install ros-melodic-desktop-full 
    echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
    sudo apt install python-rosdep
    sudo rosdep init
    rosdep update
    ```

2. Install libraries:
    ```bash
    sudo apt install ros-melodic-gps-common
    sudo apt install ros-melodic-swri-math-util
    sudo apt install ros-melodic-swri-roscpp
    sudo apt install ros-melodic-swri-serial-util
    sudo apt install ros-melodic-swri-string-util
    sudo apt install ros-melodic-swri-nodelet 
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
    echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    ```
