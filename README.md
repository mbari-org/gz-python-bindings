# gz-python-bindings

When using Gazebo Harmonic and ROS 2 Jazzy together, `gz-*` packages come from `ros-jazzy-gz-*` apt repos.
Python bindings for these packages are not distributed via apt or pip. This repository, `gz-python-bindings` builds the python
bindings and packages them up in a simple `PyPI` index url for an easy pip install.

## Prerequisites

Follow instructions for [Installing Gazebo with ROS](https://gazebosim.org/docs/harmonic/ros_installation/).

1. [Install](https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html) ROS 2 Jazzy
2. Install `ros_gz`

   ```
   sudo apt update
   sudo apt install ros-jazzy-ros-gz
   ```

3. Ensure these packages are also installed

   ```
   sudo apt update
   sudo apt install ros-jazzy-gz-sim-vendor ros-jazzy-gz-math-vendor
   ```

## Install

```
python3 -m pip install -i https://mbari-org.github.io/gz-python-bindings/simple gz-python-bindings
```

## Use

```
from gz.sim8 import *
from gz.common5 import *
from gz.math7 import *
```
