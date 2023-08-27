###coisas pra fazer antes de instalar o referee OU O FIRASIM

antes de tudo dá um
update e um upgrade por boas práticas

```bash
sudo apt-get update && sudo apt-get upgrade
```

#instalar o g++ no ubuntu

```bash
sudo apt install build-essential
```

#instale o qt5  

siga os passos aqui, crie uma conta (necessário) e faça o chmod e instale 
//pra baixar nem precisa dar wget basta clicar em cima que irá baixar, enfim faça como achar melhor 
https://download.qt.io/new_archive/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run -> versão que está lá atualmente

https://wiki.qt.io/Install_Qt_5_on_Ubuntu

depois execute os seguintes comandos
```bash
sudo apt-get install qtbase5-dev
sudo apt-get install qtdeclarative5-dev
```

#se voce fez tudo que precisava no passo anterior openGL do QT veio junto 

#vai pro /bin e faz essas coisas aqui pra instalar o protobuf (parte que mais da merda)

### Remove old versions
```bash
  sudo rm -rf /usr/include/google/protobuf
  sudo rm -rf /usr/lib/libprotobuf*
  sudo rm -rf /usr/bin/proto*
  sudo rm -rf /usr/local/include/google/protobuf
  sudo rm -rf /usr/local/lib/libprotobuf*
  sudo rm -rf /usr/local/bin/proto*
```


```bash
sudo apt-get install autoconf automake libtool curl make g++ unzip
```


### Install protoc3

```bash
#! /bin/bash
# Make sure you grab the latest version
sudo curl -OL https://github.com/google/protobuf/releases/download/v3.6.1/protoc-3.6.1-linux-x86_64.zip

# Unzip
sudo unzip protoc-3.6.1-linux-x86_64.zip -d protoc3

# Move protoc to /usr/local/bin/
sudo cp -r protoc3/bin/* /usr/local/bin/

# Move protoc3/include to /usr/local/include/
sudo cp -r protoc3/include/* /usr/local/include/

# Optional: change owner
sudo chown $USER /usr/local/bin/protoc
sudo chown -R $USER /usr/local/include/google

sudo ldconfig
```

### Install libprotobuf
```bash

# Make sure you grab the latest version
sudo curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v3.6.1/protobuf-all-3.6.1.zip

# Unzip
sudo unzip protobuf-all-3.6.1.zip -d protobuf-all
cd protobuf-all/protobuf-3.6.1

# Installation

sudo ./configure
sudo make -j 4
sudo make check
sudo make install
sudo ldconfig
```

#PRONTO :D em teoria tudo certo
#por ultimo faz isso aqui só por verificacao e safety

```bash
sudo apt-get install git build-essential cmake qt5-default libqt5opengl5-dev libgl1-mesa-dev libglu1-mesa-dev libprotobuf-dev protobuf-compiler libode-dev libboost-dev
```

agora faça o que se pede no readme do e execute tudo

https://github.com/robocin/VSSReferee/ 

lembrando que a branch é SSL-ALGUMA-COISA