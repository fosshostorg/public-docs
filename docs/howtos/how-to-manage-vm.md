# How to manage your x86 virtual instance

You can complete several tasks on your VM using the Proxmox interface. These include:

- [x] Access your virtual instance using a full SSH console (this allows direct access into the instance — perfect if you have locked yourself out, initial installs, etc.)
- [x] Reboot, shutdown, pause, and reinstall your virtual instance
- [x] View metrics and performance history (CPU, memory, network, storage, IOPS Delay, etc.)
- [x] View audit history of your virtual instance
- [x] Mount ISOs and adapters

## How to access the Proxmox Interface


We currently operate more than 15 nodes; you will know your node from your handover email. Below is an example of a node address we operate:

> https://pve01-odg1.central.fossho.st

The node's name scheme is based on the [IATA airport codes](https://en.wikipedia.org/wiki/IATA_airport_code), the type of service provided and the node number. Using the example above:

> pve = Proxmox Virtual Environment   
> 01 = Many locations have more than one hypervisor, this is hv #1
> odg1 = Odgen, Utah datacenter number 1

Current nodes:

*   pve01-lon2 (legacy node1)
*   pve02-lon2
*   pve01-lon4
*   pve01-nqt1 (legacy node2)
*   pve01-chi1 (legacy node3)
*   pve01-lax1 (legacy node4)
*   pve02-lax1 (legacy node5)
*   pve01-ams1 (legacy node7)
*   pve01-ams2 (legacy node8)
*   pve01-dfw1 (legacy node 9, 10, and 12)
*   pve01-pdx1 (legacy node11)
*   pve02-dfw1
*   pve01-odg1 (does not match airport code)
*   pve02-odg1 (does not match airport code)
*   pve01-sin1

To achieve a more secure experience, Fosshost uses Multi-Factor Authentication (MFA). We provide it through [Authelia](https://github.com/authelia/authelia). You can use any MFA client on your device to validate your login.

After logging with Authelia, you will be automatically redirected to Proxmox's interface.

![](/assets/proxmox.png)

## First login with Authelia


**When logging in with Authelia for the first time, you will have to reset your password.** This step is needed to allow you to choose a password and to associate a device with the account for the MFA.

![](/assets/authelia-reset-passwprd.png)

After resetting your password, you will need to associate a device with your account. A screen like the one below will be displayed for that.

![](/assets/authelia-reg-device.png)

That will generate a QR Code that you'll need to read with your favourite MFA client.
<figure markdown> 
![](/assets/authelia-qr-code.png)
  <figcaption>Content obfuscated for security reasons</figcaption>
</figure>


The last step is logging in with Authelia. Now, you can access Proxmox.
