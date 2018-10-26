Installing KMDICE on Windows 64-bit systems
===========================================

PLEASE FOLLOW THE VIDEO TUTORIAL: https://youtu.be/gfZZy8b222E

1. First download komodo windows `binaries <https://artifacts.supernet.org/latest/komodo/windows/>`_ and place the files in a new folder on the Desktop called kmd ('``C:\Users\YourUserName\Desktop\kmd``') .

Open a Command Prompt for the following steps.

2. Next we'll create the Komodo directory in the ``AppData`` directory.

.. code-block:: shell

	mkdir "%HOMEPATH%\AppData\Roaming\komodo"

3. Next we will create our ``komodo.conf`` file.

.. code-block:: shell

	notepad “%HOMEPATH%\AppData\Roaming\Komodo\komodo.conf”

When Notepad opens, click ``Yes`` to create the komodo.conf file. Copy the information below and paste it into Notepad.

.. code-block:: shell

	rpcuser=yourRpcUserName 
	rpcpassword=yourSecurePassword 
	daemon=1
 	rpcallowip=127.0.0.1 
	rpcbind=127.0.0.1
	server=1
	listen=1
	addnode=5.9.102.210
	addnode=78.47.196.146
	addnode=178.63.69.164
	addnode=88.198.65.74
	addnode=5.9.122.241
	addnode=144.76.94.38
	txindex=1
	maxconnections=1

After pasting, save and exit Notepad.

4. So now that you have created your ``komodo.conf`` file you are ready to download the `zk-snark proving key <https://z.cash/downloads/sprout-proving.key>`_ and `verifying key <https://z.cash/downloads/sprout-verifying.key>`_.
While the keys are downloading let's paste following command to create the directory for ZcashParams:

.. code-block:: shell

	mkdir “%HOMEPATH%\AppData\Roaming\ZcashParams”

Once the keys have finished downloading, we'll paste this command to move the keys to our newly created ZcashParams directory: 

.. code-block:: shell

	move “%HOMEPATH%\Downloads\sprout-proving.key” “%HOMEPATH%\AppData\Roaming\ZcashParams” && move “%HOMEPATH%\Downloads\sprout-verifying.key” “%HOMEPATH%\AppData\Roaming\ZcashParams”

5. Now we can run KMDICE

.. code-block:: shell

	"%HOMEPATH%\Desktop\kmd\komodod.exe -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 &"

6. Komodod should start syncing. You can check progress by running

.. code-block:: shell

	"%HOMEPATH%\Desktop\kmd\komodo-cli.exe" -ac_name=KMDICE getinfo

7. To activate CC and be able to play KMDICE you need to get a newaddress

.. code-block:: shell

        "%HOMEPATH%\Desktop\kmd\komodo-cli.exe" -ac_name=KMDICE getnewaddress

8. Validate the new address with ``validateaddress``:

.. code-block:: shell

        "%HOMEPATH%\Desktop\kmd\komodo-cli.exe" -ac_name=KMDICE validateaddress <ADDRESS>

Copy the pubkey in the ``validateaddress`` output and then stop kmdice daemon


 To stop ``komodod``, run:

.. code-block:: shell

	"%HOMEPATH%\Desktop\kmd\komodo-cli.exe" -ac_name=KMDICE stop

9. Restart KMDICE daemon with ``-pubkey`` parameter:


.. code-block:: shell

        %HOMEPATH%\Desktop\kmd\komodod.exe -ac_name=KMDICE -ac_supply=10500000 -ac_reward=2500000000 -ac_halving=210000 -ac_cc=2 -addressindex=1 -spentindex=1 -pubkey=<YOURPUBKEY> &







Downloads:

a. Windows Binaries: https://artifacts.supernet.org/latest/windows
b. Zk-snark proving keys: https://z.cash/downloads/sprout-proving.key
c. Verifying keys: https://z.cash/downloads/sprout-verifying.key
