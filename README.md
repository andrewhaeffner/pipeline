# pipeline

'''
sudo apt install autotools-dev ccache doxygen dh-autoreconf git liblapack-dev libblas-dev libgtest-dev libreadline-dev libssh2-1-dev pylint clang-format-3.8 python-autopep8 python-catkin-tools python-pip python-git python-setuptools python-termcolor python-wstool libatlas3-base --yes

sudo pip install requests
'''

- Create catkin workspace. (todo: grab important info from maplab repo.)
- Clone this repository recursively.
- Follow instructions for installing maplab and its dependencies. (todo: look at this later and see what is redundant. Perhaps make an install script.)
- catkin build
- Run pipeline with different configurations.
- Optionally download MH_01 dataset from EuRoC and run dataset.
