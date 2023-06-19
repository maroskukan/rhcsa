# RHCSA Course

- [RHCSA Course](#rhcsa-course)
  - [Introduction](#introduction)
    - [Linux](#linux)
    - [Red Hat Enterprise Linux](#red-hat-enterprise-linux)
    - [Red Hat Certified System Administrator](#red-hat-certified-system-administrator)
  - [Getting started](#getting-started)
  - [Subscription and licensing](#subscription-and-licensing)
    - [Red Hat Content Delivery Network](#red-hat-content-delivery-network)
    - [Red Hat Developer Program](#red-hat-developer-program)
    - [Red Hat Subscription Management](#red-hat-subscription-management)
  - [Perform OS installation](#perform-os-installation)
    - [Installation media](#installation-media)
    - [Standard installation](#standard-installation)
      - [Objective](#objective)
      - [Solution](#solution)
    - [References](#references)
  - [Advanced installation](#advanced-installation)
    - [Foreword](#foreword)
    - [Kickstart](#kickstart)
    - [Kickstart Customization](#kickstart-customization)
      - [Objectives](#objectives)
      - [Prerequisites](#prerequisites)
      - [Solution](#solution-1)
    - [Anaconda](#anaconda)
    - [Anaconda Customization](#anaconda-customization)
      - [Objectives](#objectives-1)
      - [Prerequisites](#prerequisites-1)
      - [Solution](#solution-2)
  - [Work with command line](#work-with-command-line)
    - [Foreword](#foreword-1)
    - [Command Line](#command-line)
    - [Shell](#shell)
    - [Terminal](#terminal)
    - [Bash](#bash)
    - [Built-in commands](#built-in-commands)
    - [Default Streams](#default-streams)
    - [History](#history)
    - [Shortcuts](#shortcuts)
    - [Substitution](#substitution)
    - [Globbing](#globbing)
    - [Variables](#variables)
    - [Functions](#functions)
    - [Conditionals](#conditionals)
    - [Loops](#loops)
    - [Coreutils](#coreutils)
    - [Useful tools](#useful-tools)
    - [Closing thoughs](#closing-thoughs)
  - [Manage files and folders](#manage-files-and-folders)
  - [Getting help](#getting-help)
  - [Edit text files](#edit-text-files)
  - [Manage users and groups](#manage-users-and-groups)
  - [Manage file system permissions](#manage-file-system-permissions)
  - [Monitor and manage processes](#monitor-and-manage-processes)
  - [Control Services and daemons](#control-services-and-daemons)
  - [Manage remote access](#manage-remote-access)
  - [Archive and transfer files](#archive-and-transfer-files)
  - [Managing software](#managing-software)
    - [System registration](#system-registration)
    - [Repositories](#repositories)
    - [Creating Repositories](#creating-repositories)
      - [Objectives](#objectives-2)
      - [Prerequisites](#prerequisites-2)
      - [Solution](#solution-3)
    - [Consuming Repositories](#consuming-repositories)
      - [Objectives](#objectives-3)
      - [Solution](#solution-4)
    - [Packages and Environment Groups](#packages-and-environment-groups)
    - [References](#references-1)
  - [Manage time and system logs](#manage-time-and-system-logs)
  - [Analyze servers](#analyze-servers)
  - [Manage networking](#manage-networking)
  - [Manage network security](#manage-network-security)
  - [Manage filesystem](#manage-filesystem)
  - [Manage network storage](#manage-network-storage)
  - [LVM and Layered Storage](#lvm-and-layered-storage)
  - [Schedule tasks](#schedule-tasks)
  - [Performance tuning](#performance-tuning)
  - [Manage SELinux security](#manage-selinux-security)
  - [Control boot process](#control-boot-process)
  - [Shell scripting](#shell-scripting)
  - [Manage containers](#manage-containers)

## Introduction

### Linux

Linux is a free and open-source operating system based on the Unix operating system. It is highly customizable and has a wide range of software available for it. It is present on a wide range of devices, from supercomputers to appliances and up to tiny IoT sensors. Linux is known for its stability, security, and performance, and thus used by millions of people worldwide. The greatest asset Linux has is its user community. In my opinion, it is worth spending some time learning Linux as it will repay you multiple times across wide range of professions.

### Red Hat Enterprise Linux

Red Hat Enterprise Linux (RHEL) is a popular operating system widely used by businesses and organizations for mission-critical applications and services. RHEL is based on the Linux kernel and is known for its stability, reliability, and security features. It comes with tools and features designed to help organizations manage their IT infrastructure. RHEL is also known for its strong support and enterprise-level technical support services. With recent policy changes in the Red Hat Developer Program, RHEL became great choice for individual developers and small shops. For these reasons, I have selected this distribution as a role model for this article.

### Red Hat Certified System Administrator

RHCSA is a popular certification to acquire because it validates the skills and knowledge required for system administration in Red Hat Enterprise Linux environments, which is has its stable presence in enterprise environments. RHCSA certification demonstrates to employers that the candidate has a strong foundation in system administration and is capable of performing various tasks efficiently and effectively. Furthermore, RHCSA certification is a prerequisite for many advanced Red Hat certifications, making it a valuable starting point for individuals looking to advance their careers in the field of Linux system administration.

[RHCSA exam objectives](https://www.redhat.com/en/services/training/ex200-red-hat-certified-system-administrator-rhcsa-exam?section=objectives) benefits us by providing an outline of the topics and objectives they need to master to pass the certification exam. It helps us focus their studies on the most important areas, and provides a structured approach to learning. The blueprint also helps us identify areas where they may need additional practice or study. By following the blueprint, we can prepare ourselves more effectively for the RHCSA certification exam and increase our chances of success. For these reasons, I have chosen this certification as a guideline for learning Linux operating system.

## Getting started

- Open source
- Linux distributions
- Red Hat Enterprise Linux

## Subscription and licensing

### Red Hat Content Delivery Network

Red Hat Content Delivery Network (CDN) is a scalable global distribution platform that hosts various software packages such as OS installation images and application files, including regular feature updates and security patches. Published packages are reviewed and signed which provides additional trust and increases overall security and integrity.

To access these resources you need to be authenticated. This is accomplished by attaching a subscription through a system registration process managed by Red Hat Subscription Management.

One of the ways how to acquire a valid subscription is to take advantage of Red Hat Developer Program.

### Red Hat Developer Program

[Red Had Developer Program Account Registration Form](https://developers.redhat.com/) is a community-driven program that provides developers access to a wide range of resources. One of the highlights that applies to our context is that it also allows individuals to register for up to 16 systems (physical or virtual) for personal use which is ideal for labs, proof-of-concepts, and small production environments without any associated cost.

The developer subscription is valid for one year, afterwards, you need to perform registration again, which is simple in practical terms means you need to agree to ToC from a license point of view and re-register systems that consumed subscriptions from the previous year.

Now that we laid out the foundation let's register for a developer account. For that, navigate to [https://developers.redhat.com/register](https://developers.redhat.com/register). Fill out and submit the registration form as illustrated below.

![Registration Part 1](/img/rhdn_01.png)

Once you verified your email address and set the cookie preference you can log in at [https://developers.redhat.com/login](https://developers.redhat.com/login).

After you log in, navigate to subscription management at [https://access.redhat.com/management](https://access.redhat.com/management). When accessed for the first time, you are required to complete your profile by selecting the account type. Make sure you chosen Personal. Finally, fill out some additional mandatory information about yourself and hit Submit button.

![Red Hat Login Account Registration Form](/img/rhdn_02.png)

Afterwards, you will be welcomed by the main subscription management screen. Here you see a breakdown of available subscriptions, manage systems, and further bugfix, enhancement, and security advisories that affect your registered systems.

### Red Hat Subscription Management

As described previously, the subscription management portal can be accessed at [https://access.redhat.com/management](https://access.redhat.com/management). 

![Red Hat Subscription Management Summary View](/img/rhsm_01.png)

There are multiple ways how you can organize your subscriptions, including using the [Simple content access](https://access.redhat.com/documentation/en-us/subscription_central/2023/html/getting_started_with_simple_content_access/con-benefits-and-limitations-of-simplecontent_assembly-simplecontent-ctxt) which is active by default or by creating [Activation Keys](https://access.redhat.com/articles/1378093). However, to keep it simple, the only information for registering a system after OS installation is the username and password used to access this portal.


## Perform OS installation

### Installation media

For Red Hat Enterprise Linux there are multiple installation images available at [Product Downloads](https://access.redhat.com/downloads). The main difference between the `Binary DVD` and `Boot ISO` images is that the Binary DVD includes additional packages and is ideal for environments without access to Internet during installation time, therefore is bigger in size. Finally, the `KVM Guest Image` can be used to create virtual machine on a KVM/QEMU hypervisor.

These are all standard installation media provided by Red Hat. If you need to create a custom installation you can leverage the [Image Builder](https://www.redhat.com/en/topics/linux/what-is-an-image-builder) tool.

### Standard installation

#### Objective

Greetings, it is your first day at your new gig, where you joined as an infrastructure consultant. Your objective, shall you accept, is to install Red Hat Enterprise Linux OS on a server that will act as a test KVM/QEMU hypervisor for the PoC environment. You received a laptop with a corporate image of Windows with Hyper-V at your disposal, which you can use as your test bed before installing it on bare metal. 

The Virtual Machine specifications are as follows:

| Settings             | Value                             |
| -------------------- | --------------------------------- |
| Name                 | rhel01                            |
| Generation           | Generation 2                      |
| Firmware             | EUFI                              |
| Secure Boot          | Enabled                           |
| Secure Boot Template | MicrosoftEUFICertificateAuthority |
| Processor            | 2                                 |
| Memory               | 4 GB                              |
| Network Adapter      | Default Switch                    |
| Virtual Hard Disk    | VHDX                              |
| Virtual Disk Size    | 50 GB                             |
| DVD Drive            | ISO Image                         |

The OS specifications are as follows:

| Settings            | Value                     |
| ------------------- | ------------------------- |
| Languange           | English (US)              |
| Hostname            | rhel01.example.com        |
| Timezone            | America/New_York          |
| Storage             | Automatic partitionioning |
| Network             | DHCP                      |
| Root Password       | D0ntUs3m3!                |
| User Name           | ansible                   |
| User Password       | L3tm3HelpYou!             |
| User Group          | wheel                     |
| Base Environment    | Server with GUI           |
| Installation Source | rhel-9.2-x86_64-dvd.iso   |

If a setting is not included in above table assume default installer selection. The registration process will be performed using `subscription-manager` after the OS installation finished.

Good luck.

#### Solution

In this solution, we will use the `Red Hat Enterprise Linux 9.2 Binary DVD` as the source for installing Red Hat Enterprise Linux as a virtual machine.

Since we are not focusing on Hyper-V specific VM deployment details, I have prepared a sample PowerShell script that automates the creation of a VM that will meet the VM specifications defined in the objectives.

```powershell
# Download the script
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/maroskukan/hypervisor-cookbook/main/hyperv/scripts/vm_create.ps1" `
                  -OutFile "vm_create.ps1"

# Execute the script, update isoPath according your environment
.\vm_create.ps1 -Name rhel01 `
                -Size S `
                -IsoPath D:\iso\rhel-9.2-x86_64-dvd.iso
```

After the virtual machine creation, a VM console will open. The installation media's GRUB2 bootloader menu is displayed.

![Virtual Machine Console Connection View](/img/hyperv_rhel_install_01.png)

Tip: You may notice that the Hyper-V VM console does not support access to hosts clipboard, however it is possible to carry out the graphical installation remotely using VNC protocol which supports this feature. In order to start VNC server in the installation environment, select the `Troubleshooting` menu entry and then `Install Red Hat Enterprise Linux 9.2 in text mode`. Once in there you will have an option to `Start VNC` server and optionally set the password.


Select the `Install Red Hat Enterprise Linux 9.2` menu entry and hit `Enter`. This will start the Anaconda Graphical installer. 

Tip: Graphical installer is presented on `TTY6` by default. The shell is available at `TTY2` by hitting `CTRL + ALT + F2`. Explore other terminals by hitting `CTRL + ALT + Fx` where `x` is the terminal number between 1 and 6. You can also use `ALT + TAB` to switch between TTYs. A careful eye may notice that these ware briefly described when the installer starts at the bottom of the screen as:

```bash
[anaconda]:main* 2:shell  3:log  4:storage-log  5:program-log
```

Once the installer loads, the **Welcome** screen is presented. We have the option to select the language.

![Welcome Screen](/img/hyperv_rhel_install_02.png)

On the **Installation Summary** screen, we select the **Installation Destination** under the System category.

![Installation Summary Screen](/img/hyperv_rhel_install_03.png)

We ensure that the one available local disk is selected and click Done.

![Installation Destination Screen](/img/hyperv_rhel_install_04.png)

On the **Installation Source** we ensure that device `sr0` is automatically selected.

![Installation Source Screen](/img/hyperv_rhel_install_05.png)

On the **Software Selection** screen we ensure that *Server with GUI* is selected.

![Software Selection Screen](/img/hyperv_rhel_install_06.png)

On **Network & Host Name** screen, we update the hostname to `rhel01.example.com` and also ensure that we receive IP configuration from DHCP.

![Network & Host Name Screen](/img/hyperv_rhel_install_07.png)

On the **Root Password** screen, we set the password and make sure that account is not locked.

![Root Password Screen](/img/hyperv_rhel_install_08.png)

On **Create User** screen, we create an additional user and ensure that he is part of the `wheel` group by checking the `Make this user administrator` option.

![Create User Screen](/img/hyperv_rhel_install_09.png)

Finally, we begin the installation.

![Installation Summary Screen](/img/hyperv_rhel_install_10.png)

Once installation completes, we will reboot the system.

![Installation Progress Screen](/img/hyperv_rhel_install_11.png)

When the reboot completes, we log in as the user we created during installation.

![Gnome Display Manager Login Screen](/img/hyperv_rhel_install_12.png)

On the Gnome Activities screen, we open the Gnome Terminal to register the system and update all installed software packages. You need to provide your Red Hat credentials created in the previous section.

![Gnome Activities Screen](/img/hyperv_rhel_install_13.png)

```bash
sudo subscription-manager register
sudo dnf update -y
```

We can verify that related Hyper-V modules and services are installed and running and that the CPU virtual extensions required for running KVM/QEMU hypervisor are available to the OS.

```bash
# List Hyper-V related modules
lsmod | grep hv_utils
hv_utils               57344  3
hv_vmbus              155648  7 hv_balloon,hv_utils,hv_netvsc,hid_hyperv,hv_storvsc,hyperv_keyboard,hyperv_drm

# List Hyper-V related services
systemctl list-units --type=service | grep Hyper-V
  hypervfcopyd.service                                  loaded active running Hyper-V FCOPY daemon
  hypervkvpd.service                                    loaded active running Hyper-V KVP daemon
  hypervvssd.service                                    loaded active running Hyper-V VSS daemon

# Validate the support Intel VT-x or AMD-V virtualization technology
grep -E 'vmx|svm' /proc/cpuinfo
```

Finally, we close the Gnome terminal and return to main desktop.

![Gnome Desktop](/img/hyperv_rhel_install_14.png)

Tip: If you don't need this Virtual Machine anymore, you can decommission it using the following PowerShell script. It will remove the VM and delete any associated leftover files. Afterwards, also you need to remove the system in Subscription management portal.

```powershell
# Download the script
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/maroskukan/hypervisor-cookbook/main/hyperv/scripts/vm_delete.ps1" `
                  -OutFile "vm_delete.ps1"

# Execute the script
.\vm_delete.ps1 -Name rhel01
```

Congratulations, you have completed all listed objectives. On top of that, you updated the system and validated that Hyper-V guest tools are working and that support for KVM/QEMU on this VM is enabled.

### References

Want to learn more about a particular program or feature used in the solution? Consult the following man pages: `systemctl(1)`, `lsmod(8)`, `grep(1)`, `subscription-manager(8)`, `dnf(8)`.


I hope you had as much fun reading this article as I had writing it. If you are hungry for more articles like this one, let me know in the comments section below.


## Advanced installation

### Foreword

The ability to automatically install Linux OS offers several benefits. Firstly, it saves significant time and effort by eliminating the need for manual installation on multiple systems, making it ideal for large-scale deployments. Secondly, it ensures consistency and accuracy in the installation process, reducing the chances of human errors. It also allows for easy replication of installations, enabling you to quickly set up new machines with predefined configurations, software packages, and security settings.

### Kickstart

Kickstart is a tool used to automate the installation of an operating system. It involves creating a configuration also referred to as an answer file that contains all the necessary settings and options for the installation, such as disk partitioning, package selection, and user accounts. The Kickstart configuration file is then used by the Anaconda installer to perform a fully automated installation without any user intervention. This saves time and reduces the potential for errors during the installation process. Kickstart is commonly used in enterprise environments where large numbers of systems need to be installed and configured quickly and efficiently.

To generate a kickstart file, we can use the [Kickstart Generator](https://access.redhat.com/labs/kickstartconfig/) or we can write your own as we will do in this article.

Tip: If you performed a manual installation described in [Installing Red Hat Enterprise Linux](https://medium.com/@maros.kukan/installing-red-hat-enterprise-linux-d8299396f5cb), then a kickstart file was automatically generated by Anaconda and stored in root's home directory as `anaconda-ks.cfg`.


### Kickstart Customization

#### Objectives

A coworker from the database team is frustrated by manual installation for Red Hat Enterprise Linux, which he performs every week. The current process is time-consuming and often produces inconsistent results. He asked for your wisdom in setting up a more advanced installation process that he could use for virtual and bare metal machines.

He is looking for a reusable configuration template, which he could leverage for automated installation for all future builds.

He shared that the provisioning network where these machines are connected offers dynamic network configuration through DHCP, but each new machine needs to have a unique hostname. He would like to have the ability to supply this value at the beginning of the installation.

For local accounts setup, besides the root account, he asked for one additional privileged user to create called `ansible` with a password of `ansible`. After the installation, his existing post-deployment script will update these local users' credentials once the machine is reachable via SSH. For software selection, he is happy with the `minimal install` installation as he will customize the software stack based on machine usage. Finally, he would like to use your private repository for the time being.

#### Prerequisites

The following prerequisites are required before you can continue with the solution:

- An existing Red Hat Enterprise Linux system setup for hosting private BaseOS and AppSteam repositories

Tip: Not sure if you meet these prerequisites? Consult the [Managing Software in Red Hat Enterprise Linux](https://medium.com/@maros.kukan/managing-software-in-red-hat-enterprise-linux-fb47d3ae2631) guide.


#### Solution


![Kickstart-1](/img/kickstart_01.png)

We start by gaining root privileges on the existing `rhel01` machine. We will use this virtual machine to generate a custom kickstart file for generic installations.

Before that, let us explore the existing kickstart file that was generated  from the answers we provided in the manual installation process described in [Installing Red Hat Enterprise Linux](https://medium.com/@maros.kukan/installing-red-hat-enterprise-linux-d8299396f5cb) guide.

Nothing is more painful than spending hours perfecting the custom kickstart file to find out that contains errors that prevent the installation process to continue. Therefore it is vital to perform validation during the development phase using `ksvalidator` which is part of `pykickstart` package.

```bash
# Intalls tools
dnf install -y pykickstart
```

Now, we are ready to validate and inspect the reference file located in `/root/anaconda-ks.cfg`. If `ksvalidator` returns no output that means no errors were found.

```bash
# Validate default ks file.
ksvalidator /root/anaconda-ks.cfg

# Inspect the reference file
cat /root/anaconda-ks.cfg | head
# Generated by Anaconda 34.25.2.10
# Generated by pykickstart v3.32
#version=RHEL9
# Use graphical install
graphical
repo --name="AppStream" --baseurl=file:///run/install/sources/mount-0000-cdrom/AppStream

%addon com_redhat_kdump --enable --reserve-mb='auto'

%end
```

Tip: If you are refactoring existing kickstart files used for older OS releases, then the `ksverdiff` might be handy. For example, to show the differences from RHEL8 to RHEL9 use the `-f` and `-t` arguments. For example `ksverdiff -f RHEL8 -t RHEL9`.

The reference kickstart file `anaconda-ks.cfg` contains roughly 45 lines. We are only going to focus on a few that concern your objectives. For a full list consult the pykickstart's official [documentation](https://pykickstart.readthedocs.io/en/latest/kickstart-docs.html).

For convenience, we start from the end. We download the final kickstart file and make it available under `ks/` folder located in the web server root directory.

```bash
mkdir -pv /var/www/html/ks
curl -o /var/www/html/ks/generic-ks.cfg \
        https://raw.githubusercontent.com/maroskukan/rhcsa/main/support/ks/generic-ks.cfg
```

Tip: Depending on the origin of this file, you might need to verify permissions and the SELinux label to be served by the web server.

Next, let us inspect this kickstart file. Concerning our objectives, there was a need to be able to take user input for the hostname and use it to adjust the configuration. We address this requirement in the `Network information` section displayed below.

```bash
grep "Network information" -A15 generic-ks.cfg
# Network information
%pre
#!/bin/bash

# Default hostname
echo "network --device eth0 --bootproto dhcp --hostname localhost.localdomain" > /tmp/network-include
# Search for hostname parameter, if found update the network ks
for args in `cat /proc/cmdline`; do
        case $args in hostname*)
            eval $args
            sed -i "s/localhost.localdomain/$hostname/g" /tmp/network-include
            ;;
        esac;
    done
%end
%include /tmp/network-include
```

We first use the [pre-installation script](https://pykickstart.readthedocs.io/en/latest/kickstart-docs.html#chapter-4-pre-installation-script) (`%pre`). where we write a default network configuration into a temporary file `/tmp/network-include`. Next, we iterate over a list of kernel arguments that are space-separated and stored in `/proc/cmdline`. When we find a match for the `hostname*` string in the list we source this key-value pair in the environment, making it available through the `$hostname` variable. When this happens, we use `sed` to update the default value for the hostname. Finally, we include this custom configuration file.

Tip: Be aware of the End of Line Sequence. If you edit these files in Windows using the `CRLF` line endings may contain special characters invisible to naked eye. This causes issues when you redirect output to a file e.g. `> /tmp/network include`. Therefore make sure you use `LF` for line endings.

The local user account credentials requirement is implemented in the following section.

```bash
grep Root -A4 generic-ks.cfg
# Root password - "redhat"
rootpw --iscrypted $6$R8s8JcJVnjPVpjrR$b3iEiZdRzC50M/5qUT9Pf1O07QfXVlKneXWyVmkFV/g2TzBdTC05ffz7dzHMiJ1CxmueCTYoE5mNpuBTk2sJ0.
# User password - "ansible"
user --groups=wheel --name=ansible --password=$6$BErsrjivm5Y.UExP$glz8qL9vfGScQT1CAr3T1WuW7pK1RBtNgQyzvomFGrRO19M/b8PXEIWAcbmjm97//KXwWx1Z.SecOrgGKAqtR0 --iscrypted --gecos="ansible"
```

We used the `mkpasswd --method=SHA-512 --stdin` to generate password hashes for both `root` and `ansible` users. We also ensure that the `ansible` user has administrative privileges by defining membership in the `wheel` supplementary group.

The package selection requirement is implemented by the following section.

```bash
grep %packages -A1 generic-ks.cfg
%packages
@^minimal-environment
```

We defined only installing the `minimal-environment` package group.

The repository definition part is implemented in the following sections.

```bash
grep https -B1 generic-ks.cfg
# Repositories
repo --name="AppStream" --noverifyssl --baseurl=https://rhel01.mshome.net/rhel9.2/x86_64/dvd/AppStream
--
# Use network installation
url --noverifyssl --url="https://rhel01.mshome.net/rhel9.2/x86_64/dvd/BaseOS/"
```

We defined custom URLs pointing to the private repositories hosted on `rhel01`. We need to disable SSL verification since we are using self-signed certificates.

That is all when it comes to the template itself. Now let us verify that it works by creating a new virtual machine.

From Hyper-V host provision a new virtual machine `rhel03`.

```powershell
# From Hyper-V Host, download the vm creation script
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/maroskukan/hypervisor-cookbook/main/hyperv/scripts/vm_create.ps1" `
                  -OutFile "vm_create.ps1"

# From Hyper-V Host, execute the script, update isoPath according to your environment
.\vm_create.ps1 -Name rhel03 `
                -Size S `
                -IsoPath D:\iso\rhel-9.2-x86_64-boot.iso
```

Once the GRUB2 menu loads, use arrows to navigate to the first menu entry labeled `Install Red Hat Enterprise Linux 9.2` and hit `e` to edit commands before booting.

Using arrows navigate the line starting with `linuxefi` and append the following three additional boot options.

```bash
inst.ks=https://rhel01.mshome.net/ks/generic-ks.cfg inst.noverifyssl hostname=rhel03
```

Tip: Looking for more information on boot options? The following [documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/performing_an_advanced_rhel_8_installation/kickstart-and-advanced-boot-options_installing-rhel-as-an-experienced-user) is great resource.


![Kickstart-2](/img/kickstart_02.png)


Afterwards, hit `CTRL + x` or `F10` to boot.

Tip: An alternative approach is to invoke the GRUB2 command line interface using `CTRL + c` and specifying the initial RAM disk (initrd) and kernel with custom parameters and then use `boot` to continue.

```bash
linuxefi /images/pxeboot/vmlinuz inst.stage2=hd:LABEL=RHEL-9-2-0-BaseOS-x86_64 quite inst.ks=https://rhel01.mshome.net/ks/generic-ks.cfg inst.noverifyssl hostname=rhel03
initrdefi /images/pxeboot/initrd.img
boot
```

When successful, you should see that the kickstart file was downloaded and validated. The installation will then begin.

![Kickstart-3](/img/kickstart_03.png)

Tip: Having trouble with Anaconda installation? Switch to shell and check logs at `/tmp/anaconda.log` By the way the the ks file is downloaded to `/run/install/ks.cfg`.

Once the installation completes and the virtual machine reboots. Verify from the Hyper-V host that the SSH service is running.

```powershell
# From Hyper-V Host, verify that the VM listens on TCP/22 (SSH)
Test-NetConnection -ComputerName "rhel03.mshome.net" `
                   -Port 22 `
                   | Select-Object -Property `
                   @{Name="ComputerName"; Expression={$_.ComputerName}}, `
                   @{Name="RemoteAddress"; Expression={$_.RemoteAddress.IPAddressToString}}, `
                   @{Name="TcpTestSucceeded"; Expression={$_.TcpTestSucceeded}} `
                   | ConvertTo-Json
```

An example of happy output would look like the following.

```json
{
  "ComputerName": "rhel03.mshome.net",
  "RemoteAddress": "172.19.102.38",
  "TcpTestSucceeded": true
}
```

In summary, we addressed all requirements received from our colleague. When done exploring the environment, we can clean up by removing the `rhel03` virtual machine.

```powershell
# From Hyper-V Host, download the vm creation script
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/maroskukan/hypervisor-cookbook/main/hyperv/scripts/vm_delete.ps1" `
                  -OutFile "vm_delete.ps1"

# From Hyper-V Host, delete the virtual machine
.\vm_delete.ps1 -name rhel03
```

### Anaconda

Anaconda is the default installer for Red Hat Enterprise Linux (RHEL) and simplifies the installation process by providing a user-friendly interface. It allows users to customize their RHEL installation, including partitioning, software packages, networking, and security settings. With automatic hardware detection and support for various storage configurations, Anaconda ensures a smooth and reliable deployment of RHEL.

### Anaconda Customization

#### Objectives

A colleague from the platform team is currently overloaded by manually deploying hundreds of new bare metal hypervisor hosts that will be used for Red Hat Virtualization. He heard about your recent contribution to the database team and how you used Kickstart to automate part of the process. He would like to go further and eliminate the need to define hostname as kernel argument manual during installation.

As he describes further, when new servers are racked, an entry in CMDB is created with their serial number and hostname. He would like to leverage information in this database to create one kickstart file that would be automatically fetched through the network by the installer during deployment. After this groundwork is completed he can focus on automating the attachment of ISO images via server Base Management Controller's Redfish API.

#### Prerequisites

The following prerequisites are required before you can continue with the solution:

- An existing Red Hat Enterprise Linux system setup for hosting private BaseOS and AppSteam repositories
- Access to RHEL BOOT ISO file

Tip: Not sure if you meet these prerequisites? Consult the [Managing Software in Red Hat Enterprise Linux](https://medium.com/@maros.kukan/managing-software-in-red-hat-enterprise-linux-fb47d3ae2631) guide.

#### Solution

![Anaconda-1](/img/anaconda_01.png)

In the first portion of this solution, we focus on custom installation ISO generation. We start by mounting the boot DVD into the existing `rhel01` virtual machine from the Windows Hyper-V host.

```powershell
# From Hyper-V Host, attach the RHEL Installation BOOT ISO to rhel01 VM
Set-VMDvdDrive -VMName rhel01 `
               -ControllerNumber 1 `
               -ControllerLocation 0 `
               -Path D:\iso\rhel-9.2-x86_64-boot.iso
```

Next, on `rhel01` we gain super user privileges by using sudo in interactive mode `sudo -i`. We verify that `/dev/cdrom` device is aware of the ISO and we mount it to `/media` mountpoint.

```bash
# From rhel01 VM, verify ISO Label
blkid /dev/cdrom
/dev/cdrom: UUID="2023-04-13-16-58-02-00" LABEL="RHEL-9-2-0-BaseOS-x86_64" TYPE="iso9660" PTUUID="54f155da" PTTYPE="dos"

# Mount DVD
mount /dev/cdrom /media
```

Next, we create directories inside the web root directory and recursively copy content from mounted DVD media.

```bash
# Create a temporary directory
tmpdir=$(mktemp -d)

# Copy all files from boot DVD to temporary directory
cp -pRf /media/* $tmpdir
```

Optionally, check out the ISO structure using `tree`.

```bash
# List the ISO structure
tree $tmpdir
/tmp/tmp.vHg3l32pCc
├── EFI
│   └── BOOT
│       ├── BOOTX64.EFI
│       ├── fonts
│       │   └── unicode.pf2
│       ├── grub.cfg
│       ├── grubx64.efi
│       └── mmx64.efi
├── images
│   ├── efiboot.img
│   ├── install.img
│   └── pxeboot
│       ├── initrd.img
│       └── vmlinuz
└── isolinux
    ├── boot.cat
    ├── boot.msg
    ├── grub.conf
    ├── initrd.img
    ├── isolinux.bin
    ├── isolinux.cfg
    ├── ldlinux.c32
    ├── libcom32.c32
    ├── libutil.c32
    ├── memtest
    ├── splash.png
    ├── vesamenu.c32
    └── vmlinuz
```

Next, we update the GRUB2 configuration file for EUFI-based systems.

```bash
# Descrease timeout from 60s to 5s
sed -i 's/set timeout=60/set timeout=5/' $tmpdir/EFI/BOOT/grub.cfg
# Update default menu entry to first one
sed -i 's/set default="1"/set default="0"/' $tmpdir/EFI/BOOT/grub.cfg
# Append inst.* kernel parameters
sed -i '/BaseOS-x86_64 quiet/ s/$/ inst.ks=https:\/\/rhel01.mshome.net\/ks\/cluster-ks.cfg inst.noverifyssl/' $tmpdir/EFI/BOOT/grub.cfg
```

Next, we update the ISOLINUX configuration file for BIOS-based systems.

```bash
# Descrease timeout from 60s to 5s
sed -i 's/timeout 600/timeout 50/' $tmpdir/isolinux/isolinux.cfg
# Update default menu entry to first one
sed -i '/^  menu default$/d' $tmpdir/isolinux/isolinux.cfg
sed -i '/menu label \^Install Red Hat Enterprise Linux 9.2/ a\  menu default' $tmpdir/isolinux/isolinux.cfg
# Append inst.* kernel parameters
sed -i '/BaseOS-x86_64 quiet/ s/$/ inst.ks=https:\/\/rhel01.mshome.net\/ks\/cluster-ks.cfg inst.noverifyssl/' $tmpdir/isolinux/isolinux.cfg
```

Tip: Looking for more information about these configuration files? Have a look at [anaconda_customization_guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/anaconda_customization_guide).

Next, we generate a new iso image.

```bash
# Install tools required to generate ISO image
dnf install -y xorriso isomd5sum

# Create ISO image
genisoimage -U -r -v -T -J -joliet-long \
            -V "RHEL-9-2-0-BaseOS-x86_64" \
            -volset "RHEL-9-2-0-BaseOS-x86_64" \
            -A "RHEL-9-2-0-BaseOS-x86_64" \
            -b isolinux/isolinux.bin \
            -c isolinux/boot.cat \
            -no-emul-boot \
            -boot-load-size 4 \
            -boot-info-table \
            -eltorito-alt-boot \
            -e images/efiboot.img \
            -no-emul-boot -o \
            /tmp/rhel-9.2-x86_64-cluster.iso \
            $tmpdir

# Optionally implant checksum that can be used when rd.live.check option is invoked
implantisomd5 /tmp/rhel-9.2-x86_64-cluster.iso
```

Next, unmount the ISO from the virtual machine and clean up the temporary build folder.

```bash
# From rhel01 virtual machine, unmount DVD
umount /media
rm -rf $tmpdir
```

Finally, disconnect the DVD from the Hyper-V host machine and download the newly generated iso image.

```powershell
# From Hyper-V host, diconnect the ISO from DVD Drive
Set-VMDvdDrive -VMName rhel01 -ControllerNumber 1 -ControllerLocation 0 -Path $null

# Download the custom ISO from rhel01 guest
scp ansible@rhel01.mshome.net:/tmp/rhel-9.2-x86_64-cluster.iso D:\iso\
```

Next, to simulate a CMDB where real serial numbers would be stored, we create three new virtual machines and note their serial numbers.

```powershell
$vmNames = "kvm01", "kvm02", "kvm03"

foreach ($vmName in $vmNames) {
    .\vm_create.ps1 -name $vmName `
                    -size S `
                    -isoPath "D:\iso\rhel-9.2-x86_64-cluster.iso" `
                    -state create
}
```

Below is an example output from the script above.

```powershell
{
  "ElementName": "kvm01",
  "BIOSSerialNumber": "6087-4370-6019-5585-3621-5785-34"
}
{
  "ElementName": "kvm02",
  "BIOSSerialNumber": "5948-8072-6590-5481-7600-8443-67"
}
{
  "ElementName": "kvm03",
  "BIOSSerialNumber": "6859-8687-6280-6177-6603-0753-51"
}
```

Next, from `rhel01` virtual machine, download and update the `/var/www/html/ks/cluster-ks.cfg` file. Using `sed`, we update the placeholders with values from the above output.

```bash
# Download the boilerplate kickstart file
curl -o /var/www/html/ks/cluster-ks.cfg \
        https://raw.githubusercontent.com/maroskukan/rhcsa/main/support/ks/cluster-ks.cfg

# Update the serial numbers for the tree VMs
sed -i 's/VM1_SN_PLACEHOLDER/6087-4370-6019-5585-3621-5785-34/' /var/www/html/ks/cluster-ks.cfg
sed -i 's/VM2_SN_PLACEHOLDER/5948-8072-6590-5481-7600-8443-67/' /var/www/html/ks/cluster-ks.cfg
sed -i 's/VM3_SN_PLACEHOLDER/6859-8687-6280-6177-6603-0753-51/' /var/www/html/ks/cluster-ks.cfg
```

From Hyper-V host shell, power on the three virtual machines using `Start-VM` wrapped in for loop.

```powershell
foreach ($vmName in $vmNames) {
    Start-VM $vmName
}
```

After a few minutes, perform a simple connection test targeting SSH.

```powershell
# From Hyper-V Host, verify if VMs listen on TCP/22 (SSH)
foreach ($vmName in $vmNames) {
  Test-NetConnection -ComputerName "$vmName.mshome.net" `
                     -Port 22 `
                     | Select-Object -Property `
                     @{Name="ComputerName"; Expression={$_.ComputerName}}, `
                     @{Name="RemoteAddress"; Expression={$_.RemoteAddress.IPAddressToString}}, `
                     @{Name="TcpTestSucceeded"; Expression={$_.TcpTestSucceeded}} `
                     | ConvertTo-Json
}
```

An example of happy output would look like the following:

```json
{
  "ComputerName": "kvm01.mshome.net",
  "RemoteAddress": "172.19.108.188",
  "TcpTestSucceeded": true
}
{
  "ComputerName": "kvm02.mshome.net",
  "RemoteAddress": "172.19.104.7",
  "TcpTestSucceeded": true
}
{
  "ComputerName": "kvm03.mshome.net",
  "RemoteAddress": "172.19.97.83",
  "TcpTestSucceeded": true
}
```

In summary, we addressed all requirements received from our colleague. When done exploring the environment, we can clean up by removing the three new virtual machine.

```powershell
foreach ($vmName in $vmNames) {
  .\vm_delete.ps1 -name $vmName
}
```

And with, we are at the end of this article. I hope you had a great time reading it. Let me know your thoughts in the comments section below.

## Work with command line

### Foreword

Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features"
-- Bell System Technical Journal

Welcome to an exciting journey into the world of Linux command line interface! Whether you are a seasoned system administrator or just starting as a DevOps engineer, mastering the bash shell opens up a realm of possibilities. In this article, we will delve into the essential techniques and best practices for interacting with the command line and explore Bash features in depth. Equipped with this knowledge, you are on the right path to streamlining your administrative tasks and unleashing the true power of Linux. Let’s dive in!

### Command Line

A command line serves as a text-based interface through which we give instructions to a computer system. In Linux, this command line is provided by a program known as the `shell`. Over time various shell program variants have been developed , offering different features and functionalities.

### Shell

A shell is a program that interprets and executes commands entered by the user. It serves as a command-line interface, providing a way to interact with the operating system. The shell takes user input, interprets the commands, and communicates with the operating system to execute them.

In Red Hat Enterprise Linux (RHEL) and many other popular Linux distributions, the GNU Bourne-Again Shell (bash) is configured as the default user shell. Bash is an enhanced iteration of the original Bourne Shell (sh) found in UNIX systems, incorporating improvements and additional features.

Tip: List of available shells is listed in /etc/shells file. We can change our default shell using chsh utility which is part of util-linux-user package.

When a shell waits for our input, it presents a string known as the shell prompt. For regular users, the shell prompt includes a concluding dollar ($) character.

```bash
[user@host ~]$
```

When the shell is running as the superuser, root, the hash (`#`) character replaces the dollar (`$`) character. This alteration serves as an indicator of a superuser shell, acting as a safeguard against potential mistakes that could impact the entire system.

```bash
[root@host ~]#
```

Leveraging bash for command execution offers immense power. With its built-in scripting language, the bash shell empowers task automation. It equips users with capabilities that enable and simplify complex operations, particularly those challenging to achieve efficiently using graphical tools, especially at scale.

Tip: There are several alternatives to the bash shell, each with its features and syntax. Some popular include [Zsh](https://zsh.sourceforge.io/), [Fish](https://fishshell.com/), and [PowerShell](https://github.com/PowerShell/PowerShell).

### Terminal

Terminal is a software application that provides a user interface to interact with the shell. It provides a window or console where users can enter commands and receive output from the shell. The terminal acts as an intermediary between the user and the shell, displaying the shell prompt and facilitating the exchange of commands and results.

A terminal can provide the following ways to access the shell:

**Physical Console**. Accessed with directly connected hardware keyboard and display. It can provide access to Virtual Console(s) also known as TTYs. By default, these are accessed using `CTRL + ALT` and a function key (`F1` through `F6`).

**Terminal Emulators**: Software applications mimicking a console interface.

**Graphical Login Prompt**: Login to a graphical environment and open a terminal program such as GNOME Terminal or Konsole.

**Remote Access**: Connect to a remote computer using SSH.

As it is impossible to cover every possible way how to interact with the system using cli, we will focus the remainder of this article on Bash shell which we access from GUI as well as remotely using SSH.

### Bash

As stated earlier, Bash is an enhanced iteration of the original Bourne Shell (sh). It was developed and released by Brian Fox in 1989 for the GNU Project. It introduced several features and improvements compared to the original Bourne Shell. These include command history, tab completion, command line editing, shell variables and functions, improved job control, conditional constructs, arithmetic operations, and more. No wonder why it became so popular.

To explore bash capabilities, we start by downloading a sample Vagrantfile, which includes a definition of a single client system running Red Hat Enterprise Linux 9.

📝Note: The following section assumes that you have completed the Hyper-V and Vagrant setup. These and many other tools are presented in the article Increase Your Output: Essential Tools Every Developer Needs!.

```powershell
# Download the Vagrantfile
$url = "https://raw.githubusercontent.com/maroskukan/rhcsa/main/Vagrantfiles/env1/Vagrantfile"
Invoke-WebRequest -Uri $url -OutFile Vagrantfile

# Start the Instance
vagrant up

# Connect to the Instance
vagrant ssh
```

You will land in shell as regular user `vagrant`. This is our starting point.

Note: The Vagrantfile template uses the `generic/rhel9` box. To keep the box file small as possible, it was installed with a minimal set of [packages](https://github.com/lavabit/robox/blob/d9bfb6bf8845e629f6d304519d9b37cb1cbe8eb9/http/generic.rhel9.vagrant.ks#LL22C10-L22C10) in mind. Therefore, to use GUI to access the shell, you need to register your system first and then install the `@gnome-desktop` package group.

We can use the `tty` command to quickly determine which terminal device has been assigned to this SSH session. In the output below, we can observe that the very first pseudo-terminal slave was assigned to our remote login session.

```bash
/dev/pts/0
```

Knowing which pseudo-terminal slave (pts) has been assigned to a user can provide several benefits, including interacting with user sessions, sending messages or notifications, monitoring user activity, and troubleshooting.

In the next section, we dive deeper into bash features and capabilities.

### Built-in commands

We start with bash built-in commands, These are built directly into the Bash shell. They provide the shell's core functionality and are available without the need for external programs or utilities. Bash built-ins provide essential functionality for working with the shell, managing the environment, and performing common operations. These built-in commands are usually faster and more efficient than external commands because they are executed directly within the shell's process.

They include commands for file and directory manipulation, variable manipulation, I/O operations, control flow, and more. Bash built-ins enhance the overall usability and power of the shell, making it a versatile and powerful tool for scripting and interactive shell sessions. For example:

File and directory manipulation.

```bash
cd /path/to/directory           # Change directory
mkdir new_directory             # Create a new directory
rm file.txt                     # Remove a file
cp file.txt destination         # Copy a file to a destination
mv file.txt new_name            # Move/rename a file
```

Variable manipulation.

```bash
variable="Hello, World!"        # Assign a value to a variable
echo $variable                  # Print the value of a variable
length=${#variable}             # Get the length of a string
```

I/O operations.

```bash
echo "Hello, World!"             # Print a string to the terminal
read -p "Enter your name: " name # Read input from the user
```

You can use the `type` command in the shell to determine if a command is a shell built-in or an external program. For example:

```bash
type cd
cd is a shell builtin

type cat
cat is /usr/bin/cat
```

Besides built-in commands many programs and utilities come from [GNU Core Utilities](https://www.gnu.org/software/coreutils/) (Coreutils). These are described later in this article.

### Default Streams

In shell programming, the default streams (`stdin`, `stdout`, and `stderr`) handle input, output, and error messages. These streams are necessary for command-line interaction, displaying results, and communicating errors.

```bash
# Search for files changed in the last hour and save the results to 'changed.txt'
# redirect any errors to sink hole
find / -type f -mmin -60 > changed.txt 2>/dev/null
```

Streams allow for the redirection of output from one program to serve as input for another using unnamed pipes. Unnamed pipes enable the seamless flow of data between commands, improving efficiency and enabling complex data processing workflows.

```bash
# Count the number of lines containing "error" in a log file
cat logfile.txt | grep "error" | wc -l
```

Additionally, named pipes, also known as FIFOs, provide a practical way to establish communication between different processes or even across systems. Named pipes act as special files that allow for inter-process communication, facilitating the exchange of data in a similar manner to unnamed pipes, but with more flexibility and persistence.

```bash
# Create a named pipe
mkfifo mypipe

# In one terminal, write data into the named pipe
echo "Hello, World!" > mypipe

# In another terminal, read data from the named pipe
cat < mypipe
```

Tip: There are several other options for inter-process communication. These include signals, shared memory, message queues, semaphores, and sockets.

Exit codes, another crucial aspect, are numeric values returned by commands upon completion. They provide information about the success or failure of a command's execution. Exit codes can be practically used in shell scripts to make decisions based on the outcome of a command. For example, conditional statements can be used to take different actions depending on whether a command succeeded or encountered an error. This allows for robust error handling and automation of tasks based on command execution outcomes.

```bash
# Check if a file exists and take action based on the result
if [ -f myfile.txt ]; then
    echo "File exists."
else
    echo "File does not exist."
fi
```

💡Tip: After command execution the exit code (status) is captured in $? variable.

In Bash, the `||` and `&&` operators are used for conditional execution of commands based on the success or failure of previous commands.

The `||` operator, also known as the OR operator, allows you to specify a command to be executed only if the previous command fails (returns a non-zero exit status). It is typically used for error handling or fallback actions. If the preceding command fails, the command following || will be executed. However, if the preceding command succeeds, the command following || will be skipped.

```bash
# Check if a directory exists, and create it if it doesn't
mkdir my_directory && echo "Directory created." || echo "Failed to create directory."

# Install a package using a package manager, and display a success message or error message
dnf install httpd && echo "Package installed." || echo "Failed to install package."
```

### History

The history feature allows us to recall and reuse previously executed commands. By default, Bash saves the command history in a file called `~/.bash_history`. This file contains a list of commands executed in previous sessions. The size of the history list is typically set to a default value, such as 500 or 1000 commands.

To view the command history, you can type the "history" command in the shell. It will display a numbered list of commands along with their execution order. You can recall a command by using its history number with the `!` symbol. For example, `!10` will execute the 10th command in the history list.

```bash
# View the command history
history

# Execute a command from history by its number
!5

# Use the history expansion to repeat the last command
!!

# Search for a specific command in history
Ctrl+R
```

To temporarily disable history in Bash and prevent sensitive information from being recorded, you can use the "set" command to modify the "HISTFILE" variable. Here's an example:

```bash
# Disable history temporarily
unset HISTFILE

# Enter sensitive information here
echo "Do not include this in history"

# Enable history again
export HISTFILE=~/.bash_history
```

### Shortcuts

Keyboard shortcuts provide a convenient way to increase productivity and efficiency when working with the command line interface. They allow you to perform common tasks and navigate through commands and text more quickly. 

Below is a list of the most useful day-to-day keyboard shortcuts:

`Ctrl+L`: Clears the screen, similar to the "clear" command.
`Ctrl+A`: Moves the cursor to the beginning of the line.
`Ctrl+E`: Moves the cursor to the end of the line.
`Ctrl+R`: Initiates a reverse search through the command history.

For working with processes these shortcuts are usefull.

`Ctrl+C`: Interrupts the currently running command or process.
`Ctrl+D`: Sends an end-of-file (EOF) signal, indicating the end of input or exiting the shell.
`Ctrl+Z`: Suspends the currently running process and puts it in the background.

And finally, we need to mention `Tab`, which auto-completes commands, file names, and directories.

Tip: In order to fully take advantage of Tab completion, make sure you have the `bash-completion` package installed.

Another useful shortcut for quickly replacing a word or phase in the previous command and re-execute it is `^^`. For example

```bash
# Check web server status
systemctl status httpd

# Below shortcut starts httpd
^status^start
```

### Substitution

Substitution is a mechanism in Bash that allows you to capture the output of a command and use it as part of another command or store it in a variable. It provides a way to dynamically incorporate command output into shell scripts or command-line operations.

There are two forms of command substitution in Bash: using backticks (``command``) and the `$()` syntax ($(command)).

Backticks (command): Backticks were the traditional way of performing command substitution in older versions of Bash. When a command is enclosed in backticks, it is executed, and the output is substituted into the command or assigned to a variable. However, backticks can be less readable, especially when nested or used within complex commands.

```bash
serial=`cat /sys/class/dmi/id/board_serial`
echo $serial
```

$() syntax ($(command)): The $() syntax is the preferred and more modern way of performing command substitution. It has become the standard method due to its improved readability and ease of use, especially in complex scenarios or nested commands.

```bash
serial=$(cat /sys/class/dmi/id/board_serial)
echo $serial
```

Both forms achieve the same result of capturing the output of a command. However, the $() syntax is generally preferred for code clarity and easier command nesting.


### Globbing

Globbing is a feature that allows you to match and expand file or directory names using wildcard characters. The most commonly used wildcard characters are `*` (matches any sequence of characters), `?` (matches any single character), and `[...]` (matches any single character within the specified range or set).

```bash
# Create three new files: file1.txt, file2.txt, file3.txt
touch file{1..3}.txt

# List only file1.txt and file2.txt
ls file[1-2].txt
```

Brace expansion is a feature that allows you to generate multiple strings or sequences by specifying a pattern enclosed within curly braces `{}`. It provides a concise way to generate and manipulate lists of strings.

```bash
# Create a backup of the bashrc file with the current date
cp ~/.bashrc{,$(date +%Y-%m-%d)}
```

### Variables

Variables store and manipulate data. They are case-sensitive and consist of letters, digits, and underscores. Assign values without spaces, like variable_name=value. Variables can store strings, numbers, and arrays, providing flexibility in scripts. Access them with $variable_name.

```bash
# Assigning simple variables
name="Bash"
age=33
country="USA"

# List
distros=("ubuntu" "fedora" "arch")

# Array
numbers=(1 2 3 4 5)

# Accessing and printing variable values
echo "Name: $name"
echo "Age: $age"
echo "Country: $country"

# Accessing and printing list elements
echo "Distributions: ${distros[@]}"
```

Besides user-defined variables, there are some well know reserved variables such as:

### Functions

Functions are used to group commands and give them a name. They improve code organization and reusability. They can accept arguments and return values. By defining functions, we can modularize our script, make it more readable, and easily reuse code.

```bash
# Define a function named "greet"
greet() {
    name="$1"
    echo "Hello, $name!"
}

# Call the function and pass an argument
greet "Maros"
```

### Conditionals

Conditionals in Bash, such as `if` statements and `case` statements, allow for making decisions and executing code based on specific conditions. They are used to control the flow of the script and enable dynamic and responsive behavior.

```bash
current_day=$(date +%A)

if [[ $current_day == "Saturday" || $current_day == "Sunday" ]]; then
    echo "It's the weekend. Writing time!"
else
    echo "It's a workday. Project time!"
fi
```

```bash
source /etc/os-release

case $ID in
    ubuntu)
        echo "This is Ubuntu."
        ;;
    fedora)
        echo "This is Fedora."
        ;;
    arch)
        echo "This is Arch Linux."
        ;;
    *)
        echo "Unknown distribution."
        ;;
esac
```

### Loops

Loops in Bash allow for repetitive tasks and iterating over values. Types of loops include `for`, `while`, and `until`. The `for` loop iterates over a sequence of values. The `while` loop repeats commands as long as a condition is true. The `until` loop continues until a condition becomes true. Loops automate tasks and process data, providing flexibility and control in script development.

```bash
servers=("server1" "server2" "server3")
for server in "${servers[@]}"; do
    echo "Checking status of $server"
    ssh "$server" systemctl status service
done
```

```bash
counter=0

while [ $counter -lt 5 ]; do
    echo "Performing system check..."
    counter=$((counter + 1))
    sleep 1
done

echo "System check completed."
```

```bash
until systemctl is-active --quiet httpd; do
    echo "Waiting for service to start..."
    sleep 5
done
echo "Service is now active!"
```

### Coreutils

GNU Core Utilities, or Coreutils, are essential command-line tools for Unix-like systems. Developed by the GNU Project, they provide a wide range of functionalities for file and directory management, text processing, and system operations. From basic operations like copying and moving files to advanced tasks like searching and manipulating file content.

Coreutils offer reliable and efficient solutions. These tools, such as `ls`, `cp`, `rm`, and `cat`, are widely used for their consistency and compatibility across different platforms, making them indispensable for effective command-line usage.

### Useful tools

[Exa](https://github.com/ogham/exa) is a modern replacement for the "ls" command in Linux and Unix-like systems. It provides a visually appealing and customizable interface for listing directory contents. With features like color-coding, different viewing modes, and additional functionalities such as filtering and sorting, Exa enhances the file listing experience in the command line. It offers improved readability and ease of use, making it a popular tool for users working with the command line.

[Bat](https://github.com/sharkdp/bat) is a command-line tool that serves as a replacement for the "cat" command in Linux and Unix-like systems. It provides syntax highlighting and other additional features, making it more versatile and user-friendly compared to the traditional "cat" command. Bat supports a wide range of file types and formats, allowing users to view file contents with syntax highlighting for improved readability. It also includes features like line numbering, Git integration, and paging, making it a powerful tool for working with text files in the command line. With its enhanced functionality and aesthetics, Bat offers a more pleasant and productive experience when viewing file contents on the command line.

[Tmux](https://github.com/tmux/tmux/wiki) is a terminal multiplexer that allows users to create and manage multiple terminal sessions within a single window. It enhances productivity and efficiency by enabling users to switch between different sessions, split the window into panes, and run multiple commands simultaneously. Tmux provides a customizable and scriptable environment, allowing users to create and save layouts, detach and reattach sessions, and share sessions with other users. It also supports session logging, copy-pasting between panes, and various window management features. Tmux is a valuable tool for developers, system administrators, and power users who work extensively in the command line, as it simplifies multitasking and organization of terminal sessions, leading to a more streamlined and productive workflow.

[JC](https://github.com/kellyjonbrazil/jc) is known as JSON Convert is modern tool which can JSONify output of many CLI tools, file-types and common strings for parsing purposes. It is module and extendable through the use of parsers. It is available as a binary or package for common Linux distributions as well pip package.

[JQ](https://github.com/jqlang/jq) is a versatile command-line tool for JSON data manipulation. It offers a powerful query language and a wide range of operations to extract, filter, and transform JSON structures. JQ's concise syntax and functional programming-inspired approach make it a preferred choice for working with complex JSON data. It is widely used by developers, sysadmins, and data engineers for tasks like data extraction, transformation, and JSON processing pipelines. With JQ, you can efficiently process JSON data from the command line, script data workflows, and integrate it into automation and data processing pipelines.

[Dasel](https://github.com/TomWright/dasel) is a command-line tool that allows you to query and modify data in various formats, including JSON, YAML, TOML, and XML. It provides a simple syntax inspired by CSS selectors for extracting, filtering, and transforming data. With Dasel, you can easily navigate hierarchical data structures, perform operations like updating and deleting data, and format the output. It's a versatile tool for tasks such as data extraction, configuration management, and automation.



### Closing thoughs

In conclusion, working with the command line in Linux provides a powerful and efficient means of interacting with the system. It offers flexibility, speed, and fine-grained control over various tasks, enabling users to perform complex operations, automate processes, and gain a deeper understanding of their system. While there may be a learning curve, the benefits of the command line far outweigh the initial challenges. I encourage further discussion in the comments section to share experiences, and tips, and explore the vast potential of the command line in the Linux ecosystem. Let's dive in, embrace the command line, and unlock a world of possibilities in our Linux journey.



## Manage files and folders

- Filesystem hierarchy
- Manage files
- Soft and hard links
- Useful tools (tree)


## Getting help

- Application argument help
- Manual Pages
- Product Documentation


## Edit text files

- Cat
- Sed
- Nano
- Vim


## Manage users and groups

- Local users and groups
- Superuser privileges
- Manage users and groups


## Manage file system permissions

- Interpret permissions
- Manage permissions
- Default permissions


## Monitor and manage processes

- Processes
- Jobs


## Control Services and daemons

- Systemd
- Control system services


## Manage remote access

- Introduction to Secure Shell
- Configure SSH Password-based authentication
- Configure SSH Key-based 
- Troubleshoot SSH Access
- Miscellaneous SSH configuration


## Archive and transfer files

- Compression and archiving
- Transfer files between systems
- Synchronize files between systems


## Managing software

As an administrator, knowing how to effectively manage software in Linux is crucial. This skill involves installing, updating, and removing packages.

Why is it essential? Firstly, it grants access to a vast range of open-source software, enhancing functionality to meet your specific requirements. Regularly updating packages safeguards against vulnerabilities and can boost system performance. 

Managing software also optimizes resources, removes unnecessary components, and enables efficient troubleshooting.

In this article, we are going to take a look at how manage software in Red Hat Enterprise Linux using practical examples.


### System registration

In Red Hat Enterprise Linux, system registration is the process of associating a specific system with a Red Hat account and subscription. It is important because it enables the system to receive software updates, security patches that are provided through the Red Hat Content Delivery Network. 

By registering a system with a Red Hat account, we can ensure that the system stays up-to-date and compliant with Red Hat's software policies and that we have access to technical support.

Therefore, before we can perform the registration we need to have a valid Red Hat account. I have explained the process for creating one in [Installing Red Hat Enterprise Linux](https://medium.com/@maros.kukan/installing-red-hat-enterprise-linux-d8299396f5cb).

There are several methods for registering a system, depending on the environment and deployment scenario. Some of the most common methods include:

- Subscription Manager Gnome application
- Subscription Manager CLI application
- RHEL Web Console
- Ansible

Subscription Manager Gnome application provides an easy to use UI for registering the system.

![Subscription Manager Gnome App](/img/smga_01.png)

Subscription Manager CLI application provides a robust framework for registering the system and managing entitlements.

```bash
subscription-manager
addons         config         --help         orgs           register       repos          syspurpose
attach         environments   identity       plugins        release        role           unregister
auto-attach    facts          import         redeem         remove         service-level  usage
clean          -h             list           refresh        repo-override  status         version
```


RHEL Web Console also know as the [Cockpit project](https://cockpit-project.org/) provides a modern way of managing server through an easy to use web console.

![RHEL Web Console Subsciption](/img/smwc_01.png)

Ansible is an open-source automation tool that simplifies IT orchestration by allowing administrators to manage and configure systems with a declarative language and a simple, agentless architecture. It has a modular architecture and provides different modules designed to interact with various parts of the system.

In the context of subscription management a sample playbook for registering a system could look like following:

```yml
---
- name: Customize managed host after initial setup
  hosts: localhost
  become: yes

  tasks:
    - name: Ensure previous subscriptions are removed
      ansible.builtin.shell: |
        subscription-manager remove --all
        subscription-manager unregister
        subscription-manager clean
      changed_when: false
      tags: ['rhsm']

    - name: Register The System into Red Hat Subscription Management
      community.general.redhat_subscription:
        state: present
        activationkey: "{{ rhsm_ak }}"
        org_id: "{{ rhsm_org }}"
      tags: ['rhsm']
```


### Repositories

Software repositories in Linux are central locations where software packages are stored and managed for distribution, allowing users to easily search, download, and install software packages. They are an important part of the Linux ecosystem, ensuring up-to-date and secure software packages.

### Creating Repositories

#### Objectives

Greetings, after your success installing the very first Red Hat Enterprise Linux in proof of concept envrionment, you have been tasked to prepare a locally hosted software repository for machines that will leverage automated installation using kickstart and much smaller boot ISO media. 

Even though this is not a production environment, your coworker, who is responsible for infrastructure security would be very happy if you keep the host firewall running and use TLS for securing data in transit. At least until he rolls out the PKI infrastructure for this company. Finally, ensure that all configuration changes are persist after a machine reboot.

Good Luck.

#### Prerequisites

The following prerequisites are required before you can continue with the solution:

- Access to registered Red Hat Enterprise Linux system
- Access to RHEL installation DVD ISO file
- Access to privileged local user account

Tip: Not sure if you meet these prerequisites? Consult the [Installing Red Hat Enterprise Linux](https://medium.com/@maros.kukan/installing-red-hat-enterprise-linux-d8299396f5cb) guide.


#### Solution

![Packages - Server](/img/packages_01.png)

We start by mounting the installation DVD into the existing rhel01 virtual machine from Windows Hyper-V host.

```powershell
Set-VMDvdDrive -VMName rhel01 -ControllerNumber 1 -ControllerLocation 0 -Path D:\iso\rhel-9.2-x86_64-dvd.iso
```

From the virtual machine console, we gain super user privileges by using sudo in interactive mode `sudo -i`. We verify that `/dev/cdrom` device is aware of the ISO and we mount it to `/media` mountpoint.


```bash
# Verify ISO Label
blkid /dev/cdrom
/dev/cdrom: UUID="2023-04-13-16-58-02-00" LABEL="RHEL-9-2-0-BaseOS-x86_64" TYPE="iso9660" PTUUID="d3d1f9a5" PTTYPE="dos"

# Mount DVD
mount /dev/cdrom /media
```

First, to configure a locally hosted package repository, we need to install and configure an Apache web server.

To secure data in transit, we need to generate a self-signed certificate and private key and update the SSL configuration file.

```bash
# Install Required Software Packages
dnf install -y httpd mod_ssl

# Generate a self-signed certificate
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/pki/tls/private/server.key -out /etc/pki/tls/certs/server.crt

# Backup and Update the Apache's SSL configuration to use certificate
cp /etc/httpd/conf.d/ssl.conf /etc/httpd/conf.d/ssl.conf.bak
sed -i 's/^Listen 443.*/Listen 443 https/g' /etc/httpd/conf.d/ssl.conf
sed -i 's/^#ServerName.*/ServerName rhel01.mshome.net/g' /etc/httpd/conf.d/ssl.conf
sed -i 's/^SSLEngine.*/SSLEngine on/g' /etc/httpd/conf.d/ssl.conf
sed -i 's/^SSLCertificateFile.*/SSLCertificateFile \/etc\/pki\/tls\/certs\/server.crt/g' /etc/httpd/conf.d/ssl.conf
sed -i 's/^SSLCertificateKeyFile.*/SSLCertificateKeyFile \/etc\/pki\/tls\/private\/server.key/g' /etc/httpd/conf.d/ssl.conf
```


Next, we need to update the firewall configuration to include the web ports.

```bash
# Update firewall configuration
firewall-cmd --add-service=http --permanent
firewall-cmd --add-service=https --permanent
firewall-cmd --reload
```


Next, we need to enable and start the Apache web service.

```bash
# Start and enable the Apache web service
systemctl enable --now httpd
```


Next, we test if the web service is working. From the Hyper-V host perform a web request to the rhel01 virtual machine.

```powershell
# Test the httpd service
curl -k https://rhel01.mshome.net
```


Next, we need to create directories inside the web root directory and recursively copy content from mounted DVD media.

```bash
# Prepare hosting directory
mkdir -pv /var/www/html/rhel9.2/x86_64/dvd/{BaseOS,AppStream}

# Copy repositories from DVD to hosting directory
cp -r /media/BaseOS/* /var/www/html/rhel9.2/x86_64/dvd/BaseOS/
cp -r /media/AppStream/* /var/www/html/rhel9.2/x86_64/dvd/AppStream/
```


Finally, unmount the ISO from the virtual machine and disconnect the DVD from the host machine.

```bash
# From rhel01 virtual machine, unmount DVD
unmount /media
```

```powershell
# From Windows Host machine, diconnect the ISO from DVD Drive
Set-VMDvdDrive -VMName rhel01 -ControllerNumber 1 -ControllerLocation 0 -Path $null
```


Tip: Another valid approach is to download Binary ISO inside the machine that will act as a repository server and mount it directly in the `/var/www/html/rhel9.2/x86_64/dvd/` directory.


Congratulations, you have completed all listed objectives. On top of that, you have updated the firewall configuration and enabled support transport layer security.

In the next section, we look at how to consume this privately hosted repository by managing configuration from the client's point of view.


### Consuming Repositories

#### Objectives

Greetings, with good words spreading fast across the campus and a colleague from the application frontend team heard about your success with setting up the first RHEL POC machine hosting a private repository. He is also very curious and wants to learn more about this "backend" stuff which is handled by your team. Therefore, he went and used your work instructions and installed his first RHEL lab machine too. To please his minimalist mindset as well as maximize his learning experience, he went with `Minimal install` when selecting software packages during installation.

After the installation, he quickly realized that his virtual machine is unable to  access the Red Hat Content Delivery Network. He suspects that it could be due to department firewall restrictions. Therefore he kindly asked you if he could leverage your private repository. He also asked you to explain how to work with RPM packages and DNF.


#### Solution

![Packages - Client](/img/packages_02.png)

To define a custom repository on a client machine, we need to create a new repo file in `/etc/yum.repos.d/` drop-in directory. We can use `cat` with redirection which is also referred to as the HEREDOC method for writing multi-line text content.

```bash
cat <<EOF > /etc/yum.repos.d/rhel_dvd.repo
[rhel-9-for-x86_64-baseos-dvd]
name=Red Hat Enterprise Linux 9.2 BaseOS (DVD)
baseurl=https://rhel01.mshome.net/rhel9.2/x86_64/dvd/BaseOS
sslverify=0
gpgcheck=1
enabled=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release

[rhel-9-for-x86_64-appstream-dvd]
name=Red Hat Enterprise Linux 9.2 AppStream (DVD)
baseurl=https://rhel01.mshome.net/rhel9.2/x86_64/dvd/AppStream
sslverify=0
gpgcheck=1
enabled=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release
EOF
```


Since we are using a self-signed certificate we need to disable the SSL verification. We can leave the GPG check enabled because we are providing packages that are signed by a trusted key.

To verify that the newly defined repositories are available we can use the `dnf repoinfo` command.

```bash
dnf repoinfo rhel-9-for-x86_64-baseos-dvd
```
```bash
Updating Subscription Management repositories.
Unable to read consumer identity

This system is not registered with an entitlement server. You can use subscription-manager to register.

Red Hat Enterprise Linux 9.2 BaseOS (DVD)                                            60 kB/s | 2.7 kB     00:00
Red Hat Enterprise Linux 9.2 AppStream (DVD)                                        108 kB/s | 3.2 kB     00:00
Repo-id            : rhel-9-for-x86_64-baseos-dvd
Repo-name          : Red Hat Enterprise Linux 9.2 BaseOS (DVD)
Repo-status        : enabled
Repo-revision      : 1681421128
Repo-updated       : Thu 13 Apr 2023 05:25:29 PM EDT
Repo-pkgs          : 1,155
Repo-available-pkgs: 1,155
Repo-size          : 1.2 G
Repo-baseurl       : https://rhel01.mshome.net/rhel9.2/x86_64/dvd/BaseOS
Repo-expire        : 172,800 second(s) (last: Fri 12 May 2023 02:13:00 PM EDT)
Repo-filename      : /etc/yum.repos.d/rhel_dvd.repo
Total packages: 1,155
```

As you can see from the above output, there are two software repositories defined.

The `BaseOS` repository is a primary software repository in Red Hat Enterprise Linux (RHEL). It consists of components and packages that serve as the foundation of the operating system. These packages encompass essential system utilities, libraries, command-line tools, and other fundamental software necessary for the proper operation of RHEL.

The `AppStream` repository consists of additional packages (applications, runtime environments, tools) which are distributed as [application streams](https://www.redhat.com/en/blog/introduction-appstreams-and-modules-red-hat-enterprise-linux). 



Now that we have the foundation laid down, let us explore various ways how we can interact with RPM software packages and its database. 

The database-related files are stored in the `/var/lib/rpm` directory. If you are curious about the database structure, make a copy and explore it using the `sqlite3` tool. You can easily list all defined tables using the query below.

```bash
dnf install -y sqlite
cp /var/lib/rpm/rpmdb.sqlite{,.bak}

# List the first three defined tables
sqlite3 /var/lib/rpm/rpmdb.sqlite.bak "SELECT name FROM sqlite_master WHERE type='table' LIMIT 3;"
Packages
sqlite_sequence
Name

# List the last three installed packages
sqlite3 /var/lib/rpm/rpmdb.sqlite.bak "SELECT key FROM Name ORDER BY hnum DESC LIMIT 3;"
tree
sqlite
gpg-pubkey
```


As you imagine, this is not the gentleman's way to interact with the local database. For that, you can employ the `rpm` command. Below are a couple of helpful queries.

```bash
# Query DB for a package that provides a file
rpm -qf /etc/passwd
setup-2.13.7-9.el9.noarch

# Query DB for a package that provides a directory
rpm -qf /dev/
filesystem-3.16-2.el9.x86_64

# Query DB for installed packages, show last 3
rpm -qa | tail -3
gpg-pubkey-5a6340b3-6229229e
sqlite-3.34.1-6.el9_1.x86_64
tree-1.8.0-10.el9.x86_64
```


To investigate an RPM package lifecycle, we need to download one first. This can be achieved by using `curl` or `dnf`.

```bash
# Download the package using wget
curl -k -o tree-1.8.0-10.el9.x86_64.rpm \
      https://rhel01.mshome.net/rhel9.2/x86_64/dvd/BaseOS/Packages/tree-1.8.0-10.el9.x86_64.rpm 

# Download the package using dnf
dnf download tree

# Install the tree package
rpm -iv tree-1.8.0-10.el9.x86_64.rpm
Verifying packages...
Preparing packages...
tree-1.8.0-10.el9.x86_64

# Query the tree package
rpm -q tree

# Erase the tree package
rpm -e tree
```


Even though we can manage packages with `rpm` it is not the recommended method. The reason is that rpm by itself can't resolve software dependencies. This is demonstrated in the example below.

```bash
curl -k -o bash-completion-2.11-4.el9.noarch.rpm \
     https://rhel01.mshome.net/rhel9.2/x86_64/dvd/BaseOS/Packages/bash-completion-2.11-4.el9.noarch.rpm

rpm -iv bash-completion-2.11-4.el9.noarch.rpm
error: Failed dependencies:
        /usr/bin/pkg-config is needed by bash-completion-1:2.11-4.el9.noarch
```


For this reason, we should leverage `dnf` to manage the software lifecycle, as it can resolve these dependencies automatically. Before we explore at this particular capability, let us dive deep into package structure first. For convenience, we download `httpd` using `dnf`.


```bash
dnf download httpd | tail -1
httpd-2.4.53-11.el9_2.4.x86_64.rpm              873 kB/s |  54 kB     00:00
```

From the filename, we can determine that the package name is `httpd`, the version is `2.4.53` release `11` for `el9_2.4`, which stands for Enterprise Linux 9, and for `x86_64` architecture. Using the `file` command, we can confirm that this file is indeed an rpm package.

```bash
file httpd-2.4.53-11.el9_2.4.x86_64.rpm
httpd-2.4.53-11.el9_2.4.x86_64.rpm: RPM v3.0 bin i386/x86_64 httpd-2.4.53-11.el9_2.4
```

Under the hood this package is really an cpio archive containing metadata, scripts and application files. We use the `rpm2cpio` command to extract the content.

```bash
rpm2cpio httpd-2.4.53-11.el9_2.4.x86_64.rpm | cpio -duim
```

A new `etc` and `usr` directories have been created in current one. This gives you an idea which files will be deployed when this package is installed.


```bash
tree -F usr | head
usr
├── lib/
│   └── systemd/
│       └── system/
│           ├── htcacheclean.service
│           ├── httpd.service
│           ├── httpd@.service
│           └── httpd.socket
├── lib64/
│   └── httpd/
```

Another way for listing package content is to use RPM with the following query.

```bash
# Query Package - list all files
rpm -qpl httpd-2.4.53-11.el9_2.4.x86_64.rpm | head -10
/etc/httpd/conf.modules.d/00-brotli.conf
/etc/httpd/conf.modules.d/00-systemd.conf
/usr/lib/.build-id
/usr/lib/.build-id/33
/usr/lib/.build-id/33/affbb88a288cb3e1990731763abd7f78a696c7
/usr/lib/.build-id/9d
/usr/lib/.build-id/9d/567552d70f45df3e1ede0d13a6a6a17c1d6096
/usr/lib/systemd/system/htcacheclean.service
/usr/lib/systemd/system/httpd.service
/usr/lib/systemd/system/httpd.socket
```

We can further filter which file types are we interested in.

```bash
# Query Package - list configuration files
rpm -qpc httpd-2.4.53-11.el9_2.4.x86_64.rpm
/etc/httpd/conf.modules.d/00-brotli.conf
/etc/httpd/conf.modules.d/00-systemd.conf

# Query Package - list documentation files
rpm -qpd httpd-2.4.53-11.el9_2.4.x86_64.rpm
/usr/share/man/man5/httpd.conf.5.gz
/usr/share/man/man8/apachectl.8.gz
/usr/share/man/man8/fcgistarter.8.gz
/usr/share/man/man8/htcacheclean.8.gz
/usr/share/man/man8/htcacheclean.service.8.gz
/usr/share/man/man8/httpd.8.gz
/usr/share/man/man8/httpd.service.8.gz
/usr/share/man/man8/httpd.socket.8.gz
/usr/share/man/man8/httpd@.service.8.gz
/usr/share/man/man8/rotatelogs.8.gz
/usr/share/man/man8/suexec.8.gz

# Query Package - list scripts
rpm -qp --scripts httpd-2.4.53-11.el9_2.4.x86_64.rpm | head -7
postinstall scriptlet (using /bin/sh):


if [ $1 -eq 1 ] && [ -x "/usr/lib/systemd/systemd-update-helper" ]; then
    # Initial installation
    /usr/lib/systemd/systemd-update-helper install-system-units httpd.service htcacheclean.service httpd.socket || :

fi
```

We can also display the summary information.

```bash
# Query Package - get information
rpm -qpi httpd-2.4.53-11.el9_2.4.x86_64.rpm
Name        : httpd
Version     : 2.4.53
Release     : 11.el9_2.4
Architecture: x86_64
Install Date: (not installed)
Group       : Unspecified
Size        : 60252
License     : ASL 2.0
Signature   : RSA/SHA256, Fri 31 Mar 2023 12:04:35 PM EDT, Key ID 199e2f91fd431d51
Source RPM  : httpd-2.4.53-11.el9_2.4.src.rpm
Build Date  : Wed 29 Mar 2023 04:11:52 PM EDT
Build Host  : x86-64-07.build.eng.rdu2.redhat.com
Packager    : Red Hat, Inc. <http://bugzilla.redhat.com/bugzilla>
Vendor      : Red Hat, Inc.
URL         : https://httpd.apache.org/
Summary     : Apache HTTP Server
Description :
The Apache HTTP Server is a powerful, efficient, and extensible
web server.
```


DNF (Dandified YUM) is a package manager and successor for the popular YUM (Yellowdog Updater, Modified). It can interact with the RPM database, packages as well as repositories. Compared to RPM it can resolve any software dependencies automatically. 

The command line utility offers many useful options, we will review some of the most common ones. 

Let us start with common file and software lookup queries.

Tip: The system used for demostrations has not been registered with entitlement server. Therefore I may filter out the first 5 lines of output with `tail -n +7`.

```bash
# Query repositories for a package that provides a file - does not need to be present on local filesystem
dnf provides /usr/share/httpd

httpd-filesystem-2.4.53-11.el9_2.4.noarch : The basic directory layout for the Apache HTTP Server
Repo        : rhel-9-for-x86_64-appstream-dvd
Matched from:
Filename    : /usr/share/httpd

# Query repositories for list of package matching pattern in name
dnf list 'httpd*'

Available Packages
httpd.x86_64               2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd
httpd-core.x86_64          2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd
httpd-devel.x86_64         2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd
httpd-filesystem.noarch    2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd
httpd-manual.noarch        2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd
httpd-tools.x86_64         2.4.53-11.el9_2.4     rhel-9-for-x86_64-appstream-dvd

# Query repositories for list of packages matching pattern in name or information
dnf search 'web server'

libcurl.x86_64 : A library for getting files from web servers
libcurl.i686 : A library for getting files from web servers
nginx.x86_64 : A high performance web server and reverse proxy server
pcp-pmda-weblog.x86_64 : Performance Co-Pilot (PCP) metrics from web server logs
python3-tornado.x86_64 : Scalable, non-blocking web server and tools

# Query repositories for a list of packages matching pattern in name, information, and description
dnf search all 'web server'
```

Next, we retrieve more information about a particular package.

```bash
# Query repositories for information about httpd package
dnf info httpd

Available Packages
Name         : httpd
Version      : 2.4.53
Release      : 11.el9_2.4
Architecture : x86_64
Size         : 54 k
Source       : httpd-2.4.53-11.el9_2.4.src.rpm
Repository   : rhel-9-for-x86_64-appstream-dvd
Summary      : Apache HTTP Server
URL          : https://httpd.apache.org/
License      : ASL 2.0
Description  : The Apache HTTP Server is a powerful, efficient, and extensible
             : web server.
```

Next, we list all files provided by a package with `repoquery` argument with `--list` option.

```bash
dnf repoquery --list httpd | tail -5
Last metadata expiration check: 0:59:42 ago on Mon 22 May 2023 03:23:36 AM EDT.
/usr/share/man/man8/httpd.service.8.gz
/usr/share/man/man8/httpd.socket.8.gz
/usr/share/man/man8/httpd@.service.8.gz
/usr/share/man/man8/rotatelogs.8.gz
/usr/share/man/man8/suexec.8.gz
```

Next, we look at managing the package lifecycle with `dnf`.

```bash
# Non-interactive installation of httpd (only showing last few lines of output)
dnf install -y httpd

Installed:
  apr-1.7.0-11.el9.x86_64                                     apr-util-1.6.1-20.el9.x86_64
  apr-util-bdb-1.6.1-20.el9.x86_64                            apr-util-openssl-1.6.1-20.el9.x86_64
  httpd-2.4.53-11.el9_2.4.x86_64                              httpd-core-2.4.53-11.el9_2.4.x86_64
  httpd-filesystem-2.4.53-11.el9_2.4.noarch                   httpd-tools-2.4.53-11.el9_2.4.x86_64
  mailcap-2.1.49-5.el9.noarch                                 mod_http2-1.15.19-4.el9_2.4.x86_64
  mod_lua-2.4.53-11.el9_2.4.x86_64                            redhat-logos-httpd-90.4-1.el9.noarch

Complete!

# Interactive reinstallation of httpd
dnf reinstall httpd

# Interactive removal of httpd
dnf remove httpd
```

Another very common operation is to update all installed packages.

```bash
# Non-interactive update of all installed packages
dnf update -y
```

Finally, let us review dnf logs and history.

```bash
# Retrieve last three lines of transaction log
tail -3 /var/log/dnf.rpm.log
2023-05-19T04:20:28-0400 SUBDEBUG Erase: apr-util-bdb-1.6.1-20.el9.x86_64
2023-05-19T04:20:28-0400 SUBDEBUG Erase: apr-1.7.0-11.el9.x86_64
2023-05-19T04:20:28-0400 SUBDEBUG Erase: apr-util-openssl-1.6.1-20.el9.x86_64

# Retrieve history in table format
dnf history 
ID     | Command line                                                  | Date and time    | Action(s)      | Altered
--------------------------------------------------------------------------------------------------------------------
     8 | remove httpd                                                  | 2023-05-19 04:20 | Removed        |   12
     7 | install -y httpd                                              | 2023-05-19 04:18 | Install        |   12  <

# Interactive rollback of transaction 8 (Removal of httpd)
dnf history undo 8
```


### Packages and Environment Groups

Before we explore metapackages let us summarize what we learned about packages. As you could see from the previous demonstration, a package is a collection of files and metadata, such as the package name, version, release number, dependencies, and other package-related information, compressed into a single file with the .rpm extension. 

Metapackages are a type of package that does not contain any software but rather serve as a way to group related packages together. Metapackages are useful for managing complex software environments or software stacks, where it is important to ensure that all the required packages are installed and kept up to date. Installing a metapackage will install all of the packages that are associated with it, simplifying the process of managing software dependencies.

To list packages that are part of a metapackage we can use the `repoquery` argument with `--requires` option.

```bash
dnf repoquery --requires container-tools
```

```bash
Updating Subscription Management repositories.
Last metadata expiration check: 2:35:57 ago on Fri 12 May 2023 06:59:55 AM EDT.
(container-selinux >= 2:2.162.1 if selinux-policy)
aardvark-dns
buildah
buildah >= 1.21.4
cockpit-podman
conmon
containernetworking-plugins
containers-common
crun >= 0.19
fuse-overlayfs
netavark
oci-runtime
podman
podman >= 3.2.3
podman-docker
podman-manpages
podman-remote
python3-podman
skopeo
skopeo >= 1:1.3.1
slirp4netns
toolbox
udica
```

Environmental groups are collections of packages and package groups tailored for specific use cases, such as workstations or servers, and make it easy to install required packages and dependencies.

As with individual packages, `dnf` can be used to retrieve information about groups. We can list them by using the following `grouplist` argument.

```bash
dnf grouplist
```

```bash
Updating Subscription Management repositories.
Last metadata expiration check: 2:29:09 ago on Fri 12 May 2023 06:59:55 AM EDT.
Available Environment Groups:
   Server
   Minimal Install
   Workstation
   Custom Operating System
   Virtualization Host
Installed Environment Groups:
   Server with GUI
Installed Groups:
   Container Management
   Headless Management
Available Groups:
   Legacy UNIX Compatibility
   System Tools
   Security Tools
   Console Internet Tools
   Network Servers
   RPM Development Tools
   Development Tools
   Smart Card Support
   Graphical Administration Tools
   Scientific Support
   .NET Development
```

To list packages that are part of a group we can use the `info` argument.

```bash
dnf group info "security tools"
```

```bash
Updating Subscription Management repositories.
Last metadata expiration check: 2:31:10 ago on Fri 12 May 2023 06:59:55 AM EDT.
Group: Security Tools
 Description: Security tools for integrity and trust verification.
 Default Packages:
   scap-security-guide
 Optional Packages:
   aide
   hmaccalc
   openscap
   openscap-engine-sce
   openscap-utils
   scap-security-guide-doc
   scap-workbench
   tpm2-tools
   tss2
   udica
```

I had a blast writing this article, and I hope you had one while reading it. Hungry for more articles like this? Let me know in the comments section below.


### References 

Want to learn more about a particular program or feature used in the solution? Consult the following man pages:

rpm(8), rpm2cpio(8), cpio(1), rpmkeys(8)



## Manage time and system logs

- Manage system time
- System log architecture
- Syslog
- Journald


## Analyze servers

- System resources
- Diagnostic report
- Red Hat Insights


## Manage networking

- Networking concepts
- Network validation
- Network configuration
- Network troubleshooting
- Hostname and name resolution


## Manage network security

- Manage firewall
- Manage SELinux port labeling


## Manage filesystem

- Devices, partitions and file Systems
- Common file system types
- Create file systems
- Mount and unmount file systems
- Manage Swap
- Locate files


## Manage network storage

- Introduction to NFS
- Mounting network storage
- Automount


## LVM and Layered Storage

- Introduction to LVM
- Managing LVM
- Introduction to Stratis


## Schedule tasks

- Manage one time user jobs
- Manage recurring user jobs
- Manage recurring system jobs
- Manage temporary files  


## Performance tuning

- Manage tuning profiles
- Manage process scheduling


## Manage SELinux security

- Introduction to SELinux
- Manage SELinux mode
- Manage SELinux file contexts
- Manage SELinux policy
- Troubleshoot SELinux


## Control boot process

- Review boot process
- Configure boot target
- Reset root password
- Troubleshoot boot issues
- Manage boot loader


## Shell scripting

- Introduction to scripting
- Conditions
- Loops
- Regular expressions


## Manage containers

- Introduction to containers
- Manage basic containers
- Manage container storage
- Manage container networking
- Manage containers as services
