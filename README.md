VoteChain
==========

> WARNING: VoteChain is intended for experimenting and learning, NOT for a production environment.

![Image of VoteChain](http://)

VoteChain is your very own Blockchain as a Service that operates as a cloud voting prototype.
 
This version of VoteChain runs on [Multichain 2.0-alpha-2](https://github.com/MultiChain).




System Requirements
-------------------

To set up VoteChain, you will need 1 server (min 2 GB RAM, 2 CPUs) 
running Ubuntu 16.04.3 x64 and php 7.0. 


Installation
------------

This section presumes that you have root access to the server mentioned above and want to install chainzZz for all users on the system.

**Step 1.** Install git and clone the chainzZz repository

    sudo apt-get install git
    sudo git clone https://github.com/davidcopperfield-magicman/VoteChain.git

**Step 2.** Harden the base operating system (Ubuntu 16.04.3 x64). This will also create a new user called [yobiuser] with the password entered by you below.

    cd VoteChain
    sudo bash -e hardening.sh <password>

**Step 3.** Install the FTP server. This will set up the FTP server. For logging in, use the IP address of your server as the `host`. The username and password are as entered by you below. The connection is `SFTP`.

    sudo bash -e ftp.sh <username> <password>


**Step 4.** Install, configure and run the Multichain blockchain, Multichain web-demo and Multichain Exporer. 
This also sets up HashChain, Vault, Contracts and WebWallet. 

The RPC port will be set as `15590` and the Network port will be set as `61172`. 

If you get a "locale error" using Terminal on mac, go to Terminal -> Preferences -> Profiles and uncheck "Set locale environment variables on startup"

    sudo bash -e multichain.sh <chain-name> <rpc-username> <rpc-password>
		
*To access Multichain web-demo, visit `http://<IP Address>/multichain-web-demo`

*To access Multichain Exporer, visit `http://<IP Address>:2750`

**To use VoteChain, see the instructions at [https://github.com/Primechain/hashchain/blob/master/README.md](https://github.com/Primechain/hashchain/blob/master/README.md)



Notes
-----

This will:
1. harden the base operating system against cyber attacks

2. set up a Multichain blockchain using a pre-defined configuration

3. set up an FTP server

4. set up Multichain web demo

5. set up Multichain Explorer

9. set up WebWallet, a simple blockchain powered wallet for Yourcoins, a smart asset.

In case something goes wrong, you can roll back the multichain installation using

    bash rollback_multichain.sh 



Live demo → Update these upon completion & sucessfully running services!
---------
* To access a live Multichain web-demo, visit http://52.172.209.229/multichain-web-demo

* To access a live Multichain Exporer, visit http://52.172.209.229:2750

* To access the yobiapps, visit: http://52.172.209.229/yobiapps

