# How to manage your virtual instance

If you have requested Proxmox access to manage your virtual instance, well done! You are now on your way to having complete control over your virtual instance.

You can complete several tasks using the Proxmox interface. These include:

*   Access your virtual instance using a full SSH console (this allows direct access into the instance — perfect if you have locked yourself out, initial installs, etc.)
*   Reboot, shutdown, pause, and reinstall your virtual instance
*   View metrics and performance history (CPU, memory, network, storage, IOPS Delay, etc.)
*   View audit history of your virtual instance
*   Mount ISOs and adapters

## How to access the Proxmox Interface


We currently operate ten nodes; you will know your node from your handover email or instance hostname. Below is an example of a node address we operate:

> https://dfwhv0.central.fossho.st

The node's name scheme is based on the [IATA airport codes](https://en.wikipedia.org/wiki/IATA_airport_code), the type of service provided and the node number. Using the example above:

> dfw = Dallas/Fort Worth International Airport  
> hv = Hypervisor  
> 0 = First server on that location/provider/facility

Current nodes:

*   lonhv0 (legacy node1)
*   nqthv0 (legacy node2)
*   chihv0 (legacy node3)
*   laxhv0 (legacy node4)
*   laxhv1 (legacy node5)
*   amshv0 (legacy node7)
*   amshv1 (legacy node8)
*   dfwhv0 (legacy node 9, 10, and 12)
*   pdxhv0 (legacy node11)
*   dfwhv1

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