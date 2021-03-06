# KadiCoin

**KadiCoin**, yet another cryptocurrency. **KadiCoin** was born in **Kadikoy, Turkiye** where a group of friends meet at Kadikoy.<br>This is an experimental project and I hope it will be a good beginning in our research and development activity.

# Installation

Operating System:<br>
[Ubuntu Server 16.04.3 LTS](https://www.ubuntu.com/download/server)

**Install Prerequisities**<br><br>

sudo apt-get -y update<br>
sudo apt-get -y upgrade<br>

\# You may need to reboot your system after upgrade<br>

sudo apt-get install -y wget<br>
sudo apt-get install -y curl<br>
sudo apt-get install -y git<br>
sudo apt-get install -y build-essential<br>
sudo apt-get install -y autoconf<br>
sudo apt-get install -y automake<br>
sudo apt-get install -y libtool<br>
sudo apt-get install -y pkg-config<br>
sudo apt-get install -y libevent-dev<br>
sudo add-apt-repository ppa:bitcoin/bitcoin<br>
sudo apt-get update<br>
sudo apt-get install -y libdb4.8-dev libdb4.8++-dev<br>
sudo apt-get install -y libboost-all-dev<br>
sudo apt-get install -y libssl-dev<br>
sudo apt-get install -y libzmq3-dev<br>
sudo apt-get install -y qdbus qmlscene qt5-default qt5-qmake qttools5-dev-tools qtbase5-dev-tools qtchooser qtdeclarative5-dev xbitmaps xterm libqt5svg5-dev qttools5-dev qtscript5-dev qtdeclarative5-folderlistmodel-plugin qtdeclarative5-controls-plugin<br>

**Install libsodium Using a Workaround**<br><br>
wget http://de.archive.ubuntu.com/ubuntu/pool/universe/libs/libsodium/libsodium-dev_1.0.13-1_amd64.deb<br>
wget http://de.archive.ubuntu.com/ubuntu/pool/universe/libs/libsodium/libsodium18_1.0.13-1_amd64.deb<br>
sudo dpkg -i libsodium*deb<br>
rm libsodium18_1.0.13-1_amd64.deb<br>
rm libsodium-dev_1.0.13-1_amd64.deb<br>

**Get Source Code from GitHub and Build**<br><br>
git clone https://github.com/gokhankocak/KadiCoin.git<br>
cd KadiCoin<br>
./autogen.sh<br>
./configure<br>
make<br>
sudo make install<br>

**Create Config File**<br><br>
mkdir ~/.KadiCoin<br>
cd ~/.KadiCoin<br>
nano KadiCoin.conf<br>

**Sample KadiCoin.conf**<br><br>
\# Online Config Generator:<br>
\# https://jlopp.github.io/bitcoin-core-config-generator/

server=1<br>
\# Bind to given address and always listen on it. Use [host]:port notation for IPv6. Replace it with your own IP.<br>
\# bind=192.168.0.26<br>

\# Specify a non-default location to store blockchain and other data.<br>
\# datadir=/data<br>

\# Run this node on the Bitcoin Test Network.<br>
testnet=1<br>

\# Run this node on its own independent test network.<br>
\# regtest=1<br>

\# Username for JSON-RPC connections<br>
rpcuser=kadicoinrpcuser<br>

\# Password for JSON-RPC connections<br>
rpcpassword=PgJBtsFHuZ383n8.kp3M7g<br>

**Run KadiCoind**<br><br>
KadiCoind -printtoconsole<br>

