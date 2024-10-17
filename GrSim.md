At first 

```sh
git clone https://github.com/RoboCup-SSL/grSim.git
sudo apt install git build-essential cmake pkg-config qtbase5-dev \
                   libqt5opengl5-dev libgl1-mesa-dev libglu1-mesa-dev \
                   libprotobuf-dev protobuf-compiler libode-dev libboost-dev
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr/local ..
make
```

Now return to main folder, to run:
`sudo ./bin/grSim`
to control some robots there's the example 
`sudo ./bin/client`
