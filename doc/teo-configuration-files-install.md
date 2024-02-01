## teo-configuration-files: Installation from Source Code

First install the dependencies:

- [Install CMake 3.12+](https://github.com/roboticslab-uc3m/installation-guides/blob/master/docs/install-cmake.md)
- [Install YCM 0.11+](https://github.com/roboticslab-uc3m/installation-guides/blob/master/docs/install-ycm.md)
- [Install YARP 3.7+](https://github.com/roboticslab-uc3m/installation-guides/blob/master/docs/install-yarp.md)

### Install the Configuration files

Our software integrates the previous dependencies. Note that you will be prompted for your password upon using '''sudo''' a couple of times:

```bash
cd  # go home
mkdir -p repos; cd repos # make $HOME/repos if it does not exist; then, enter it
git clone https://github.com/roboticslab-uc3m/teo-configuration-files.git # download teo-configuration-files software from the repository
cd teo-configuration-files; mkdir build; cd build
cmake .. # configure the teo-configuration-files software
make -j$(nproc) # Compile
sudo make install # Install :-)
cd # go home
```

For CMake `find_package(TEO_CONFIGURATION_FILES REQUIRED)`, you may also be interested in adding the following to your `~/.bashrc` or `~/.profile`:
```bash
export TEO_CONFIGURATION_FILES_DIR=/path/to/teo-configuration-files/build
```

For additional `teo-configuration-files` options use ccmake instead of cmake.
