# Installing

Clone the repository and go to the most recent branch 
```bash
git clone https://github.com/robocin/vss-vision
cd vss-vision/
git checkout new-pattern
```
Install docker

Please, install docker [here:](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04)

## Dependecies
```
Qt5
OpenCV
SFML
TBB
Protobuf
```
## Running with docker
1. Build the vss-vision image using the shell script
```shell
./docker_build
```

2. Running from the docker image using the shell script
```shell
./docker_run [camera device id]
```
The camera device id should be the id found on /dev/video{id} of the camera which you want to use on vss-vision, if none is given, the image will run without a camera device attached.
The configuration files are stored on a docker volume named vss-vision-config, so the config files should persist over docker runs
## Building (Ubuntu 22.04 LTS)

1. Install the needed dependencies.
```bash
./InstallDependencies
```

2. Build via CMake
```bash
# From repository root
mkdir build
cd build
cmake ..
make
```
3. Running:
```bash
# From repository root
cd src
./VSS-VISION
```
