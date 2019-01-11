Install KMDICE using Agama Native Wallet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

First step to get KMDICE running natively in Agama is to download latest Agama release:

`Download Agama Wallet <https://komodoplatform.com/komodo-wallets/>`_


After downloading Agama for your preferred OS, run it and select ``Activate Coin``:

.. image:: http://i.imgur.com/Bga3lso.png
	:alt: Agama-login 

On the dialog box that pups up, start typing KMDICE and then select the ``Native Mode`` option, then press ``Activate Coin``: 

.. image:: http://i.imgur.com/bX8NYuD.png
	:alt: Agama-select-coin

Once the chain syncs completely you can jump to ``Receive`` screen in the wallet and look for the address that has KMDICE (if you dont, then deposit some KMDICE to an address) and then select ``copy pubkey``:

.. image:: http://i.imgur.com/E6OhRBV.png
	:alt: Agama-copy-pubkey

Then in the upper right corner of the screen select to go to ``Settings``:

.. image:: http://i.imgur.com/vkNHKDu.png
	:alt: Agama-settings

In settings, expand the ``App Config (config.json)`` section:

.. image:: http://i.imgur.com/Sb7Mexy.png
	:alt: agama-config

Scroll down to the end of the ``App Config`` section and paste the ``pubkey`` you copied before into the ``Pubkey`` setting's box, then press ``validate pubkey``, then press ``save app config``:

.. image:: http://i.imgur.com/Btbh3kr.png
	:alt: agama-config-pubkey
	
After this step you can now restart the app. When logging in again please select the option to ``use pubkey``:

.. image:: http://i.imgur.com/g3kdiSA.png
	:alt: agama-use-pubkey
	
	
And that is all, now you will able to play KMDICE from any KMDICE GUI available.
