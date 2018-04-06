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

This section presumes that you have root access to the server mentioned above and want to install VoteChain for all users on the system.

**Step 1.** Install git and clone the VoteChain repository

    sudo apt-get install git
    sudo git clone https://github.com/davidcopperfield-magicman/VoteChain.git

**Step 2.** Harden the base operating system (Ubuntu 16.04.3 x64). This will also create a new user called [youruser] with the password entered by you below.

    cd VoteChain
    sudo bash -e hardening.sh <password>

**Step 3.** Install, configure and run the Multichain blockchain and Multichain Exporer. 
This also sets up the Vote App. 

The RPC port will be set as `15590` and the Network port will be set as `61172`. 


    sudo bash -e multichain.sh <chain-name> <rpc-username> <rpc-password>

*To access Multichain Exporer, visit `http://<IP Address>:2750`

**To use VoteChain, see the instructions at [https://gitpitch.com/user/repo](https://gitpitch.com/user/repo)



Notes
-----

This will:
1. harden the base operating system against cyber attacks

2. set up a Multichain blockchain using a pre-defined configuration

3. set up an FTP server

4. set up Multichain web demo

5. set up Multichain Explorer

6. set up Vote App, a simple blockchain powered app for voting.




Live demo
---------

* To access a live VoteChain Demo Exporer, visit http://198.23.196.54:2750/

* To access the VoteApp Demo, visit: http://voteapp.gq

