# FIRASim - INSTALL

## Overview

## Dependencies

FIRASim depends on:

- [CMake](https://cmake.org/) version 3.5+ 
- [OpenGL](https://www.opengl.org)
- [Qt5 Development Libraries](https://www.qt.io)
- [Open Dynamics Engine (ODE)](http://www.ode.org)
- [VarTypes Library](https://github.com/jpfeltracco/vartypes) forked from [Szi's Vartypes](https://github.com/szi/vartypes)
- [Google Protobuf 3](https://github.com/google/protobuf)
- [Boost development libraries](http://www.boost.org/) (needed by VarTypes)

**Note:** It's necessary to compile ODE in double precision. This is default when installing the ODE binaries in Ubuntu. However, if you are compiling ODE from source (e.g on Mac OS), please make sure to enable the double precision during the configuration step: `./configure --enable-double-precision`.

### Linux/Unix Installation

If you run a Debian system, or derivative, first ensure that these dependencies are there:

```bash
sudo apt-get install git build-essential cmake qt5-default mesa-common-dev libqt5opengl5-dev libgl1-mesa-dev libglu1-mesa-dev libprotobuf-dev protobuf-compiler libode-dev libboost-dev freeglut3-dev libfontconfig1
sudo apt-get -y install cmake
sudo apt-get install libglu1-mesa-dev -y
sudo update-mime-database /usr/share/mime
```

Install VarTypes from source.

```bash
$ cd /tmp
$ git clone https://github.com/jpfeltracco/vartypes.git
$ cd vartypes
$ mkdir build
$ cd build
$ cmake ..
$ make
$ sudo make install
```

Installing QT5

```
wget https://download.qt.io/new_archive/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run
chmod +x qt-opensource-linux-x64-5.7.0.run ./qt-opensource-linux-x64-5.7.0.run
```

QT5 Requirements

If you have any problem follow this link [QT Wiki](https://wiki.qt.io/Install_Qt_5_on_Ubuntu)

At last execute this:
```bash
sudo apt-get install qtbase5-dev
sudo apt-get install qtdeclarative5-dev
```

Installing protobuf-all-3.12.4

```bash

curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v3.12.4/protobuf-all-3.12.4.tar.gz

tar -xf protobuf-all-3.12.4.tar.gz

cd protobuf-3.12.4/

./autogen.sh
./configure
make
make check
sudo make install
sudo ldconfig 
```

Next, clone FIRASim into your preferred location.

```bash
$ cd /path/to/firasim_ws
$ git clone https://github.com/IEEEVSS/FIRASim.git
$ cd FIRASim
```

Create a build directory within the project:

```bash
$ mkdir build
$ cd build
```

Run CMake to generate the makefiles:

```bash
cmake ..
```

Then compile the program:

```bash
make
```

