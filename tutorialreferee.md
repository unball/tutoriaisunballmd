# Coisas do referee

Tente executar um comando por linha pra se der erro ao menos saber o que foi.

Antes de tudo atualize suas libs, é uma boa prática

```bash
sudo apt-get update && sudo apt-get upgrade
```
## Intalação dos requisitos

### Instalação do g++ no ubuntu

```bash
sudo apt install build-essential
```

### Instalação do qt5

```
wget https://download.qt.io/new_archive/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run
chmod +x qt-opensource-linux-x64-5.7.0.run ./qt-opensource-linux-x64-5.7.0.run
```

Para o funcionamento do qt5

```
sudo apt-get install build-essential
sudo apt-get install libfontconfig1
sudo apt-get install mesa-common-dev
sudo apt-get install libglu1-mesa-dev -y
sudo update-mime-database /usr/share/mime
```
Caso tenha dado problema acesse a [Wiki do QT](https://wiki.qt.io/Install_Qt_5_on_Ubuntu)

Depois execute os seguintes comandos:
```bash
sudo apt-get install qtbase5-dev
sudo apt-get install qtdeclarative5-dev
```

Se você fez tudo que precisava no passo anterior openGL do QT veio junto 

```bash
sudo apt-get install autoconf automake libtool curl make g++ unzip
```

### Instalação do protobuf-all-3.12.4

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

## PRONTO :D em teoria tudo certo

Por último faz isso aqui só por verificação e safety

```bash
sudo apt-get install git build-essential cmake qt5-default libqt5opengl5-dev libgl1-mesa-dev libglu1-mesa-dev libprotobuf-dev protobuf-compiler libode-dev libboost-dev
```

Agora faça um clone do respositório do [VSSReferee](https://github.com/robocin/VSSReferee/) do e execute tudo

Lembrando que a branch é ```SSL-VISION-PACKETS```

```bash
git clone https://github.com/robocin/VSSReferee.git
cd VSSReferee/
git checkout LARC2023
mkdir build && cd build
qmake ..
make //here u can put the -j6 if u have a good processor
```

