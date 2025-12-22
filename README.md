# Install the C++ library

The following steps are mostly the same on all supported platforms, with some variations.

Choose a directory for installing the C++ library of RDK and its dependencies. This directory can be under system path or not, depending on whether you want RDK to be globally discoverable by CMake. For example, a new folder named rdk_install under the home directory.

1. Choose a directory for installing `flexiv_rdk` library and all its dependencies. For example, a new folder named `rdk_install` under the home directory: `~/rdk_install`. Compile and install to the installation directory:

  ```bash
  cd ~/ros2_ws/src/flexiv_ros2/flexiv_controller/flexiv_rdk/thirdparty
  bash build_and_install_dependencies.sh ~/rdk_install
  ```

2. Configure and install `flexiv_rdk`:

  ```bash
  cd ~/ros2_ws/src/flexiv_ros2/flexiv_controller/flexiv_rdk/rdk
  mkdir build && cd build
  cmake .. -DCMAKE_INSTALL_PREFIX=~/rdk_install
  cmake --build . --target install --config Release
  ```
