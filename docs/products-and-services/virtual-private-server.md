# x86 Virtual Private Server


When applying for our services, you can specify your preferred [region](/general/regions). This will typically be chosen on the following basis (this is not prescriptive):

*   The regions that your project operates in, whether in-country or global;
*   Your audience;
*   The performance from your location to the node you are considering working with/on;
*   The type of hosting you require (not all regions are available for certain services);
*   Whether there are any laws or regulations that apply;
*   Whether you require IPv6 connectivity;
*   The speeds of the connectivity of the node.

We cannot make the above decisions for you, however, we can guide you. If you would like assistance with this, please [contact us](https://fosshost.org/contact).

## VPS Specification

Each project will have the opportunity to request a VM specification during the application process. The providing of the specification is subject to availability.

## Operating Systems

We support the most common operating systems:

*   Rocky Linux;
*   Debian;
*   Ubuntu;
*   ArchLinux;
*   FreeBSD

If the operating system you are looking to use is not listed, we support custom ones. You will need to specify your OS preference during the application form by providing a URL to the ISO file. Please note that if you are thinking of using a non-standard “exotic” operating system, we will be limited in what support we can offer. There are many, and we do not know them all well.

## Network


We don't operate DHCP on our network; we only support static networking, be it IPv4, IPv6 or both. The network information for your VPS will be provided to you in the handover email and is up to you to configure it. We can, however, within our capacity, provide you with some support.

## Full Virtualization Technology (KVM)


Software called a hypervisor separates resources from their physical machines, so they can be partitioned and dedicated to VMs. When a user issues a VM instruction that requires additional resources from the physical environment, the hypervisor relays the request to the physical system and caches the changes. VMs look and act like physical servers, which can multiply the drawbacks of application dependencies and large OS footprints — a footprint that's mostly not needed to run a single app or microservice.

The KVM delivery is best suited for those looking to run docker containers, intensive applications, or need semi-dedicated hardware for development and production use.
