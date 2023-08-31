###coisas pra fazer antes de instalar o referee

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

```bash
sudo apt-get install autoconf automake libtool curl make g++ unzip
```

### Install protobuf-all-3.12.4

```bash

curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v3.12.4/protobuf-all-3.12.4.tar.gz

tar -xf protobuf-all-3.6.1.tar.gz

cd protobuf-3.12.4/

./autogen.sh

cd src/

./configure
make
make check
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
```bash
git checkout branch-name
```

```bash
mkdir build && cd build
qmake ..
make -j6
```

