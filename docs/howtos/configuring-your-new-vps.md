# Configuring your new Virtual Private Server

All projects are expected to have a reasonable understanding and system admin knowledge of Linux/\*nix systems. We do not provide off-the-shelf virtual instances which are pre-loaded with an operating system ready to go. This is because we feel that building your server should be done your way, not our way. Our understanding is that projects prefer the ability to have full autonomy rather than predefined templates or scripts. Furthermore, we will provide limited support during OS build stage, but you are expected to know what you are doing.

There are some important considerations when building your VPS, which we have detailed below:

*   You will need to use the virtual console to manage your instance;
*   You will need to have an understanding of Linux/\*nix sysadmin;
*   We do not operate DHCP.  You must therefore configure a static IPv4/IPv6 address;
*   You can use your own DNS servers or Public DNS servers. We do NOT provide DNS servers for resolv.conf;
*   It is ultimately your responsibility to install and configure the OS — we only provide the network and resources;
*   Support is available if you get stuck;
*   We do not provide hardware firewalling, however, our carriers provide basic and limited DDoS protection;
*   You must configure SSH and [secure](/howtos/how-to-lock-down-ssh) it as this is NOT our responsibility. Again, help is available if you get stuck;
*   If your allocated resources, once your server is built, does not appear to be adequate, please raise a ticket and we will see what we can do.