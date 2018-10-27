# pipeline


- Install ROS Kinetic.
- Install maplab framework dependencies:
```
sudo apt install autotools-dev ccache doxygen dh-autoreconf git liblapack-dev libblas-dev libgtest-dev libreadline-dev libssh2-1-dev pylint clang-format-3.8 python-autopep8 python-catkin-tools python-pip python-git python-setuptools python-termcolor python-wstool libatlas3-base --yes

sudo pip install requests
```

- Install ccache:
```
sudo apt install -y ccache &&\
echo 'export PATH="/usr/lib/ccache:$PATH"' | tee -a ~/.bashrc &&\
source ~/.bashrc && echo $PATH
ccache --max-size=10G
```

- Create catkin workspace (if none exists.) For example:
```
export ROS_VERSION=kinetic #(Ubuntu 16.04: kinetic, Ubuntu 14.04: indigo)
export CATKIN_WS=~/maplab_ws
mkdir -p $CATKIN_WS/src
cd $CATKIN_WS
catkin init
catkin config --merge-devel # Necessary for catkin_tools >= 0.4.
catkin config --extend /opt/ros/$ROS_VERSION
catkin config --cmake-args -DCMAKE_BUILD_TYPE=Release
cd src
```

- Clone this repository recursively in the src directory:
```
cd src
git clone <this-respository.git> --recursive
```

- catkin build:
```
catkin build maplab ???rovioli???
```

- Run pipeline with different configurations.
- Optionally download MH_01 dataset from EuRoC and run dataset.
