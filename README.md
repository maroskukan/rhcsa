# RHCSA Course

- [RHCSA Course](#rhcsa-course)
  - [Introduction](#introduction)
    - [Linux](#linux)
    - [Red Hat Enterprise Linux](#red-hat-enterprise-linux)
    - [Red Hat Certified System Administrator](#red-hat-certified-system-administrator)
  - [Tools and environment](#tools-and-environment)
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
    - [Advanced installation](#advanced-installation)
  - [Work with command line](#work-with-command-line)
  - [Manage files and folders](#manage-files-and-folders)
  - [Getting help](#getting-help)
  - [Edit text files](#edit-text-files)
  - [Manage users and groups](#manage-users-and-groups)
  - [Manage file system permissions](#manage-file-system-permissions)
  - [Monitor and manage processes](#monitor-and-manage-processes)
  - [Control Services and daemons](#control-services-and-daemons)
  - [Manage remote access](#manage-remote-access)
  - [Archive and transfer files](#archive-and-transfer-files)
  - [Managing software packages](#managing-software-packages)
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


## Tools and environment

- Hypervisor
- Vagrant
- Environments
- Extras


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

I hope you had as much fun reading this article as I had writing it. If you are hungry for more articles like this one, let me know in the comments section below.


### Advanced installation


## Work with command line

- Understanding TTYs
- Accessing CLI from GUI
- Globbing
- STDIN, STDOUT, STDERR
- Redirection
- Coreutils
- Useful tools (grep,tmux,jq,dasel)


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


## Managing software packages

- System registration
- RPM
- DNF
- Repositories
- Packages and Environment Groups


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




...jason's list
...productivity tools
