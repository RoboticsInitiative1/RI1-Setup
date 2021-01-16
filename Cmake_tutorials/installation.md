## Guide for Cmake based Installations

### General installation of cmake based packages

### Install `Cmake` commandline [Ubuntu 20.04]
```shell
sudo apt install cmake
```

### Install `Cmake-gui` [Ubuntu 20.04]
> Use the following tutorial for Cmake GUI installation from Ubuntu snap store
> [Cmake-Gui-Install-Guide](https://www.fosslinux.com/38392/how-to-install-cmake-on-ubuntu.htm)

### Make your package workspace
```shell
mkdir -p package_dev/install
cd package_dev
```

### Get the package from github or other sources
```shell
git clone <pckage_url>
# or use some other method
```

## Let your package name is `initial_pkg`

### Create a custom package install directory
```shell
# This directory will be used as install prefix for cmake 
# Your packages will be installed in here.
mkdir -p install/initial_pkg
```

```shell
# go inside the package directory
cd initial_pkg

# Create a build directory 
mkdir build && cd build
```

### Use cmake to configure your package
```shell
cmake -DCMAKE_INSTALL_PREFIX= /home/shivam/package_dev/install/initial_pkg ..
# ".." is used to specify that your cmake based configure files are in previous directory.
# -DCMAKE_INSTALL_PREFIX option will set the package install directory as specified.
```

### Build and Install the package
```shell
# Build package
make -j4

# Install package
make install
```