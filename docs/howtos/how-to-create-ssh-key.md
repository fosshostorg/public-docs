# How to create an SSH public key


**For security reasons we only handover VMs using** **an** **SSH public key configuration**, so you will need to set up an SSH key before you apply. This is a much more secure and modern alternative to connecting using a password.

Follow one of the instructions listed below to create an SSH key, according to your needs.

### Keep backward compatibility with older SSH clients

```bash
ssh-keygen -t rsa -b 4096
```

### Use a stronger cypher without backward compatibility with older SSH clients

```bash
ssh-keygen -t ed25519
```

You will be prompted to save and name the key:

> Generating public/private RSA key pair. Enter file in which to save the key (/Users/USER/.ssh/id\_rsa):

Next, you will be asked to create and confirm a passphrase for the key (highly recommended):

> Enter passphrase (empty for no passphrase):   
> Enter same passphrase again:

This will generate two files, by default called id\_rsa and id\_rsa.pub. Copy and paste the contents of the **.pub** file, typically id\_rsa.pub, into your application.