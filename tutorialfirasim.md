# FIRASim - Instalação

## Dependências

### Instação de Dependências

```bash
sudo apt-get install git build-essential cmake qt5-default mesa-common-dev libqt5opengl5-dev libgl1-mesa-dev libglu1-mesa-dev libprotobuf-dev protobuf-compiler libode-dev libboost-dev freeglut3-dev libfontconfig1
sudo apt install libode-dev
sudo apt-get -y install cmake
sudo apt-get install libglu1-mesa-dev -y
sudo update-mime-database /usr/share/mime
```

Install VarTypes de uma fork de um membro do VSSS.

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

#### Installing QT5 (Passo não necessário caso já tenha feito a instalação do Referee)

```
wget https://download.qt.io/new_archive/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run
chmod +x qt-opensource-linux-x64-5.7.0.run ./qt-opensource-linux-x64-5.7.0.run
```

Qualquer problema vá para o sequinte link [QT Wiki](https://wiki.qt.io/Install_Qt_5_on_Ubuntu)

Por fim, execute:
```bash
sudo apt-get install qtbase5-dev
sudo apt-get install qtdeclarative5-dev
```

#### Instalando o protobuf-all-3.12.4 (Passo não necessário caso já tenha feito a instalação do Referee)

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

Por fim, clone o FIRASim into your preferred location.

```bash
cd /path_to_firasim
git clone https://github.com/IEEEVSS/FIRASim.git
cd FIRASim
```

Compile o FiraSim

```bash
mkdir build
cd build
cmake ..
make
```

