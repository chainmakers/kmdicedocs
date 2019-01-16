Sign multisig transaction in Agama
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

First step to sign a multisig transaction in Agama is to download latest Agama release:

`Download Agama Wallet <https://komodoplatform.com/komodo-wallets/>`_


After downloading Agama for your preferred OS, run it and select ``Activate Coin``:

.. image:: http://i.imgur.com/Bga3lso.png
	:alt: Agama-login 

After you activate your favorite coin in lite mode, go to ``Tools`` section and select ``Multi signature transaction``

.. image:: http://i.imgur.com/8gtFoI2.png
	:alt: Agama-sign-multisig
  
**IMPORTANT**: A multisig address is a special address that will require different people to sign each transaction with their own private keys. To create a multisig transaction you will need all your peers to sign the transaction before it gets broadcasted. To sign the transaction, each peer will need the ``private key (WIF)`` of the ``pubkey`` that used to create the multisig address which can be found here:

..image:: http://i.imgur.com/jkxxl4U.png
  :alt: Agama-copy-wif

In ``Multi signature transaction`` you will select the coin used for the multisig address, input the multisig address ``redeem script``, the ``private key`` of the signer's address and the multisig address funds will move from.

.. image:: http://i.imgur.com/mxEo26V.png
	:alt: generate-multisig

Once you generate the multisig address you will get several outputs:

**Address**: ``bQE41eaXq2eC2jWtM95XqWe8TRNF8uVjv5``

**Redeem script**: ``522102c28ba9fc9c7575d0148d731bf9c9b8e4df5bc38588f5944c773c8a9ecfd1f4782102a02f2b7904381bcc0b53a701ed69a3c68a7f4ee5c35dbedca329ca6c05203b202102cbbdfa609054a88515359e91b5ebcb45fade232c104365ff3459cee74abcbee853ae``

**Script pub key**: ``a9147e1adc17cf2c33f516b222b83eb4f8f53e088a0887``

**and finally the complete script you will need to use for future transactions**:

``{"redeemScript":"522102c28ba9fc9c7575d0148d731bf9c9b8e4df5bc38588f5944c773c8a9ecfd1f4782102a02f2b7904381bcc0b53a701ed69a3c68a7f4ee5c35dbedca329ca6c05203b202102cbbdfa609054a88515359e91b5ebcb45fade232c104365ff3459cee74abcbee853ae","scriptPubKey":"a9147e1adc17cf2c33f516b222b83eb4f8f53e088a0887","nOfN":"2-3","messageSecret":"438e24da3db1407e040d86ab8462750e9125448994909d29407937931c076d53","messageCID":"040d86ab8462750e438e24da3db1407e","pubKeys":["02c28ba9fc9c7575d0148d731bf9c9b8e4df5bc38588f5944c773c8a9ecfd1f478","02a02f2b7904381bcc0b53a701ed69a3c68a7f4ee5c35dbedca329ca6c05203b20","02cbbdfa609054a88515359e91b5ebcb45fade232c104365ff3459cee74abcbee8"]}``


**IMPORTANT**: **Store this information as well as possible, you can distribute it between your peer signers so that each one can store this information. This will be vital in the capability of moving funds from this address.**

Now you have a multisig address with no funds in it. Please go to ``Multi-signature transaction`` section to be able to send from the multisig address.


