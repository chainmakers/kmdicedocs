**Installing KMDICE on Ubuntu/Debian**
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Requirements**

Currently, you will need:

- Linux (easiest with a Debian-based distribution)
- 64-bit
- 4GB of free memory


**Get Started**

Log in as the user to your system, and issue these commands to make sure your Linux machine is up to date.

.. code-block:: shell

        sudo apt-get update
        sudo apt-get upgrade  (and say Y when it wants to upgrade stuff)


**Install the dependency packages:**

.. code-block:: shell

         sudo apt-get install build-essential pkg-config libc6-dev m4 g++-multilib autoconf libtool ncurses-dev unzip git python zlib1g-dev wget bsdmainutils automake libboost-all-dev libssl-dev libprotobuf-dev protobuf-compiler libgtest-dev libqt4-dev libqrencode-dev libdb++-dev ntp ntpdate vim software-properties-common curl libcurl4-gnutls-dev cmake clang`


**Installing Komodo**

.. code-block:: shell

        cd ~
        git clone https://github.com/jl777/komodo
        cd komodo
        git checkout jl777
        ./zcutil/fetch-params.sh -j8``  uses 8 threads - replace 8 with number of threads you want to use or `nproc` variable
        ./zcutil/build.sh -j$(nproc)


This can take some time.


Now you can start `KMDICE` daemon to sync with the network

.. code-block:: shell
        
        cd ~
        cd komodo
        ./src/komodod -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 &

You might see some outputs in terminal where you started KMDICE daemon. 

**Activating CC in  KMDICE**

To play KMDICE you need to run the daemon with the ``-pubkey=`` parameter. 

First, you need to get a new address

.. code-block:: shell
	
	./komodo-cli -ac_name=KMDICE getnewaddress

Second you need to validate the address to get the pubkey

.. code-block:: shell

	./komodo-cli -ac_name=KMDICE validateaddress <ADDRESS>


And lastly, after you copy the pubkey from the output of ``validateaddress`` you can now stop the daemon and restart it with the ```-pubkey=``` parameter.


.. code-block:: shell

	./komodo-cli -ac_name=KMDICE stop
	./src/komodod -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 -pubkey=<YOUR PUBKEY> &


Now you will be able to play the game using ``dicebet``.
