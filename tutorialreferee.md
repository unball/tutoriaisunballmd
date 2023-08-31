# Coisas do referee

Tente executar um comando por linha pra se der erro ao menos saber o que foi

antes de tudo dá um
update e um upgrade por boas práticas

```bash
sudo apt-get update && sudo apt-get upgrade
```
#instalar requisitos

#instalar o g++ no ubuntu

```bash
sudo apt install build-essential
```

#instale o qt5

```
wget https://download.qt.io/new_archive/qt/5.7/5.7.0/qt-opensource-linux-x64-5.7.0.run
chmod +x qt-opensource-linux-x64-5.7.0.run ./qt-opensource-linux-x64-5.7.0.run

#para o funcionamento do qt5
sudo apt-get install build-essential
sudo apt-get install libfontconfig1
sudo apt-get install mesa-common-dev
sudo apt-get install libglu1-mesa-dev -y
sudo update-mime-database /usr/share/mime
```
caso tenha dado problema acesse: https://wiki.qt.io/Install_Qt_5_on_Ubuntu

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

tar -xf protobuf-all-3.12.4.tar.gz

cd protobuf-3.12.4/

./autogen.sh
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

agora faça o que dê um git clone vssreferee do e execute tudo
https://github.com/robocin/VSSReferee/

lembrando que a branch é SSL-VISION-PACKETS

```bash
git clone https://github.com/robocin/VSSReferee.git
git checkout SSL-VISION-PACKETS
```

```bash
cd VSSReferee/
mkdir build && cd build
qmake ..
make -j6
```

