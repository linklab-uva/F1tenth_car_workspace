### RangeLibc

This library provides for different implementations of 2D raycasting for 2D occupancy grids, including the Compressed Directional Distance Transform (CDDT) algorithm as proposed in [this publication](http://arxiv.org/abs/1705.01167). The code is written and optimized in C++, and Python wrappers are also provided.

### Building the Code

To install this on the Jetson TX2, follow the instructions below:

First, build the code locally
```
user@ros-robot: cd range_libc
user@ros-robot: mkdir build
user@ros-robot: cmake ..
user@ros-robot: make
```

To install python bindings, you need cython. Use the following command to install cython:
```
user@ros-robot: sudo apt-get install Cython
```

Install GPU-enabled python wrappers
```
user@ros-robot: cd range_libc/pywrapper
user@ros-robot: sudo WITH_CUDA=ON python setup.py install
```
