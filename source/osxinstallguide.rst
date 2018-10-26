
Installing KMDICE on OSX
^^^^^^^^^^^^^^^^^^^^^^^^

**Requirements**

Packages are installed through homebrew, make sure to install it:
 
.. code-block:: shell

        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"


Now install the dependency packages:

.. code-block:: shell

         brew tap discoteq/discoteq; brew install flock
         brew install autoconf autogen automake
         brew install gcc@6
         brew install binutils
         brew install protobuf
         brew install coreutils
         brew install wget
         brew install nanomsg


or


.. code-block:: shell

	brew tap discoteq/discoteq; brew install flock autoconf autogen automake gcc6 binutils protobuf coreutils wget nanomsg


**Clone the Komodo repository**


.. code-block:: shell

	git clone https://github.com/KomodoPlatform/komodo


**Get the proving keys:**


.. code-block:: shell

	cd komodo
	./zcutil/fetch-params.sh


**And now build Komodo**


.. code-block:: shell

	git checkout dev
	./zcutil/build-mac.sh


**Run Komodo**

If the build went well, run KMDICE:

.. code-block:: shell

	cd ~/komodo/src
	./komodod -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 &


**Get PUBKEY to use Crypto Conditions Dice Game:**

.. code-block:: shell

	./komodo-cli -ac_name=KMDICE getnewaddress


This command should print a new KMDICE address, copy that address and validate it:


.. code-block:: shell

	./komodo-cli -ac_name=KMDICE validateaddress <ADDRESS>


In the output of `validateaddress` you will see a field that says `pubkey`. You need to copy that pubkey and use it to run the daemon with it:


.. code-block:: shell

	./komodo-cli -ac_name=KMDICE stop


Now restart the daemon using the `-pubkey` parameter:


.. code-block:: shell

	./komodod -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 -pubkey=<YOUR PUBKEY>


That is all, you should now be able to play dice game.
