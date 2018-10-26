*******
dicebet
*******

Bet on the KMDICE Contract
========================

Usage:
------

``dicebet name fundingtxid amount odds``

Terminology:
------------

::

    name = Name of the Dice contract you want to place your bet  
    fundingtxid = The ID of the Dice contract  
    amount = Amount you want to place bet  
    odds = Specify your odds

Step 1: Set your parameters to create a raw transaction and get the hex value
=============================================================================

Example Command:
----------------

.. code-block:: shell

    ./komodo-cli -ac_name=KMDICE dicebet KMDICE 5be49570c56d036abb08b6d084da93a8a86f58fc48db4a1086be95540d752d6f 7 7

Output:
-------

.. code-block:: shell

	  "result": "success",
  "hex": "01000000022ec0090a3353ff185e0d98dc044c0fd36057582ef77b7f1137893c07c68585cc000000007b4c79a276a072a26ba067a5658021039d966927cfdadab3ee6c56da63c21f17ea753dde4b3dfd41487103e24b27e94e8140e24d9df4e245a9f47088b0b7f0218ee39e79a8a1c6e400f70f38fa77863ed3be6148d416d4f4c6363fceeb612f3684757c00df6afb089c05fa9358e8308f323ba100af038001e6a10001ffffffff6c7705c954b99baf63eab1a179460ab539c5fb3808e75edd777a505ae7606f57030000004847304402203d115dce3a7f7735e139a6fe2866c61422b2e0c50234ff39f690899f5bd6075d02207f2d6b939c3b021a22c0dc4a86d36427525ec41a291d8ea6c9a2b36d3e830f1a01ffffffff05201efaaf61010000302ea22c80200095ece5eee67e1f313e7ba2d156c7617106cd52b75c93ed3fb110ff3fba6e998103120c008203000401cc0027b92900000000302ea22c80200095ece5eee67e1f313e7ba2d156c7617106cd52b75c93ed3fb110ff3fba6e998103120c008203000401cc1727000000000000232102a02f2b7904381bcc0b53a701ed69a3c68a7f4ee5c35dbedca329ca6c05203b20ac6a5b347700000000232102a02f2b7904381bcc0b53a701ed69a3c68a7f4ee5c35dbedca329ca6c05203b20ac00000000000000006d6a4c6ae6424b4d4449434500006f2d750d5495be86104adb48fc586fa8a893da84d0b608bb6a036dc57095e45b4519bb670131dc318940726fab8d53e5ea2105e645b98b234365fbe9196317ad000000000000000000000000000000000000000000000000000000000000000000000000"
}

