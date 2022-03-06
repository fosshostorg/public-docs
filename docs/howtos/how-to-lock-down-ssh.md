# How to lock down SSH


It is important to lock down SSH so that it can be only accessed using a public SSH key. If you don't know how to create an SSH key, take a look [here](/howtos/how-to-create-ssh-key) to learn how to create one.

It is your responsibility to modify your SSH configuration by removing plain password authentication, changing the SSH port to lock it down and disabling root login. We do not recommend leaving plain password authentication open because it will be targeted with attacks to force entry. If you absolutely and cannot use public keys, you must consider using fail2ban or a similar tool to limit password guesses.

Typically, most Linux/\*BSD operating systems will all have a sshd\_config and, although there are some minor variations, they are typically the same for a standard distribution. Please note that we cannot capture and produce docs for each operating system, so you must use the following as a guide only. If you need specific assistance with a more exotic operating system, please contact us.

## How to access the sshd\_config


Log into your server and, through the command-line, use the following commands (using nano as a text editor):

```bash
cd /etc/ssh
nano sshd\_config
```
Use ctrl +x to exit nano, you will be asked to save your changes "Save modified buffer?" and you type 'y' (for yes - you can enter 'n' or 'c' to quit and make no changes) 

### Disable Root log in

Once you have connected to your server and created an unprivileged account that you have verified works with SSH, you can disable root logins by setting the `_PermitRootLogin no_` directive in _/etc/ssh/sshd\_config_ on your server and then restarting the server’s SSH process with a command like `_sudo systemctl restart sshd_`.

### Limit which users can log in

When having more than a user account, it is advisable to limit which accounts can log in via SSH. This configuration can be achieved in the _/etc/ssh/sshd\_conf_ file by setting up the `AllowUsers` directive and then restarting the server’s SSH process with a command like `_sudo systemctl restart sshd_`. An example follows:

```
AllowUsers alice bob
```

### Disable version 1 of the SSH Protocol (when applicable)

Some operating systems provide support to version 1 of the SSH Protocol. This protocol is no longer considered secure so, unless you can't connect to your server with the version 2 of the SSH Protocol, please force the use of the secure version in the _/etc/ssh/sshd\_config_ file with the `Protocol` directive and then restarting the server’s SSH process with a command like `_sudo systemctl restart sshd_`. Example:

```
# Protocol 2,1  
Protocol 2
```
## Securing SSH Keys


It is recommended to properly secure each user SSH keys so that other users in the system can't access them. You can do this by changing the permissions of the _$HOME/.ssh_ folder and of the ssh private and public keys. The following example shows how to do it:

```bash
cd $HOME

chmod 700 ~/.ssh
 
chmod 644 ~/.ssh/authorized\_keys

chmod 644 ~/.ssh/known\_hosts

chmod 600 ~/.ssh/private\_key

chmod 644 ~/.ssh/public\_key.pub
```