Install KMDICE using Agama Native Wallet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

First step to get KMDICE running natively in Agama is to download latest Agama release:

`Download Agama Wallet <https://komodoplatform.com/komodo-wallets/>`_


After downloading Agama for your preferred OS, run it and select ``Activate Coin``:

.. image:: http://imgur.com/5x0cDZdl.png
	:alt: Agama-login 

On the dialog box that pups up, start typing KMDICE and then select the ``Native Mode`` option, then press ``Activate Coin``: 

.. image:: http://imgur.com/ISdUo29l.png
	:alt: Agama-select-coin

Once the chain syncs completely you can jump to ``Receive`` screen in the wallet and look for the address that has KMDICE (if you dont, then deposit some KMDICE to an address) and then select ``copy pub key``:

.. image:: http://imgur.com/2pURVAOl.png
	:alt: Agama-copy-pubkey

Then in the upper right corner of the screen select to go to ``Settings``:

.. image:: http://imgur.com/D6bkbN3l.png
	:alt: Agama-settings

In settings, expand the ``App Config (config.json)`` section:

.. image:: http://imgur.com/qkrskE0l.png
	:alt: agama-config

Scroll down to the end of the ``App Config`` section and paste the ``pubkey`` you copied before into the ``Pubkey`` setting's box.
