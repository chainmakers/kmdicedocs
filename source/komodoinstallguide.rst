**Installing Komodo on Ubuntu/Debian**
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Requirements**

Currently, you will need:

- Linux (easiest with a Debian-based distribution)
- 64-bit
- 4GB of free memory


**Get Started**

Log in as the user to your system, and issue these commands to make sure your Linux machine is up to date.

``sudo apt-get update``

``sudo apt-get upgrade``  (and say Y when it wants to upgrade stuff)

**Install the dependency packages:**


```sudo apt-get install build-essential pkg-config libc6-dev m4 g++-multilib autoconf libtool ncurses-dev unzip git python zlib1g-dev wget bsdmainutils automake libboost-all-dev libssl-dev libprotobuf-dev protobuf-compiler libgtest-dev libqt4-dev libqrencode-dev libdb++-dev ntp ntpdate vim software-properties-common curl libcurl4-gnutls-dev cmake clang```

**Install nanomsg**

**Linux**


``cd ~``

``git clone https://github.com/nanomsg/nanomsg``

``cd nanomsg``

``cmake . -DNN_TESTS=OFF -DNN_ENABLE_DOC=OFF``

``make -j2``

``sudo make install``

``sudo ldconfig``


This takes some time depending your internet connection. Let it run in the background.
Now it is time to install Komodo. Follow each line step by step and ignore the "libgmp headers missing" at some point!

**Installing Komodo**

``cd ~``

``git clone https://github.com/jl777/komodo``

``cd komodo``

``git checkout beta``

``./zcutil/fetch-params.sh -j8``  uses 8 threads - replace 8 with number of threads you want to use or `nproc` variable`

``./zcutil/build.sh -j$(nproc)``


This can take some time.


Now you can start `KMDICE` daemon to sync with the network

``cd ~``

``cd komodo``

``./src/komodod -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 &``

You might see some outputs in terminal where you started `KMDICE` daemon. 
