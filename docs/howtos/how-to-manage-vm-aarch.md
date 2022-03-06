# How to manage your aarch64 virtual instance

If you have requested Proxmox access to manage your virtual instance, well done! You are now on your way to having complete control over your virtual instance.

You can complete several tasks using the Proxmox interface. These include:

*   Access your virtual instance using a full SSH console (this allows direct access into the instance — perfect if you have locked yourself out, initial installs, etc.)
*   Reboot, shutdown, pause, and reinstall your virtual instance
*   View metrics and performance history (CPU, memory, network, storage, IOPS Delay, etc.)
*   View audit history of your virtual instance
*   Mount ISOs and adapters

## How to access the Proxmox Interface


We currently operate ten nodes; you will know your node from your handover email or instance hostname. Below is an example of a node address we operate:

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
*   pve01-odg1
*   pve02-odg1
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
