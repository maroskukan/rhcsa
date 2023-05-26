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
    - [References](#references)
    - [Advanced installation](#advanced-installation)
      - [Objective](#objective-1)
      - [Solution](#solution-1)
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
  - [Managing software](#managing-software)
    - [System registration](#system-registration)
    - [Repositories](#repositories)
    - [Creating Repositories](#creating-repositories)
      - [Objectives](#objectives)
      - [Prerequsites](#prerequsites)
      - [Solution](#solution-2)
    - [Consuming Repositories](#consuming-repositories)
      - [Objectives](#objectives-1)
      - [Solution](#solution-3)
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

### References 

Want to learn more about a particular program or feature used in the solution? Consult the following man pages: `systemctl(1)`, `lsmod(8)`, `grep(1)`, `subscription-manager(8)`, `dnf(8)`.


I hope you had as much fun reading this article as I had writing it. If you are hungry for more articles like this one, let me know in the comments section below.


### Advanced installation

Kickstart is a tool used to automate the installation of operating system. It involves creating a configuration also referred to as answer file that contains all the necessary settings and options for the installation, such as disk partitioning, package selection, and user accounts. The Kickstart configuration file is then used by Anaconda installer to perform a fully automated installation without any user intervention. This saves time and reduces the potential for errors during the installation process. Kickstart is commonly used in enterprise environments where large numbers of systems need to be installed and configured quickly and efficiently.

In order to generate a kickstart file you can use the [Kickstart Generator](https://access.redhat.com/labs/kickstartconfig/). 

Tip: If you performed a manual installation described in Standard Installation section, then a kickstart file was automatically generated by Anaconda and stored in root's home directory as `anaconda-ks.cfg`.


#### Objective

#### Solution





```powershell
# Crete a virtual environment
pyenv-win-venv install 3.11.1 rhcsa
pyenv-venv activate rhcsa

# Install required packages
pip install pykickstart createrepo-c

# Validate kickstart file
ksvalidator support/rhel01-ls.cfg

# Identify differences between ks for 8 and 9
ksverdiff -f RHEL8 -t RHEL9
```

Use two processes :8000 will server ks files, :8001 will server DVD files we will be using minimal iso to kickstart the process

```powershell
# Start a simple web server instance - hosts kickstart file
python3 -m http.server 8000 --directory support
```



Below requires addtional work by creating an actual software repository - likely tools availabe in linux environment only...

```powershell
# Mount Disk Image
Mount-DiskImage -ImagePath "D:\iso\rhel-9.2-x86_64-dvd.iso"

# Retrieve assigned drive letter
$isoDrive = (Get-Volume | Where-Object {$_.FileSystemLabel -eq "RHEL-9-2-0-BaseO"} | Select-Object -ExpandProperty DriveLetter)

# Add copy operation and createrepo ops

# Start a simple web server instance - hosts files from dvd
python3 -m http.server 8001 --directory ${isoDrive}:\
```

```powershell
# Download the script
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/maroskukan/hypervisor-cookbook/main/hyperv/scripts/vm_create.ps1" `
                  -OutFile "vm_create.ps1"

# Execute the script, update isoPath according your environment
.\vm_create.ps1 -Name rhel03 `
                -Size S `
                -IsoPath D:\iso\rhel-9.2-x86_64-boot.iso
```

Once Grub2, edit the menu entry by appending the following pamater to line starting with linuxefi.

```bash
# Kernel Parameter
inst.ks=http://rhel01.mshome.net/ks/rhel03-ks.cfg
```

Tip: Anaconda downlaods the ks file to /run/install/ks.cfg and stores logs at /tmp/anaconda.log. Kernel log is at.

https://pykickstart.readthedocs.io/en/latest/kickstart-docs.html

```powershell
# Stop simple web server
Stop-Process -Name python3 -Force

# Unmount Disk Image
Dismount-DiskImage -ImagePath "D:\iso\rhel-9.2-x86_64-dvd.iso"
```


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


## Managing software

As an administrator, knowing how to effectively manage software in Linux is crucial. This skill involves installing, updating, and removing packages.

Why is it essential? Firstly, it grants access to a vast range of open-source software, enhancing functionality to meet specific requirements. Regularly updating packages safeguards against vulnerabilities and boosts system performance. 

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


RHEL web console also know as the Cockpit project provides a modern way of managing server through an easy to use web console.

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

#### Prerequsites

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

The database-related files are stored in the `/var/lib/rpm/` directory. If you are curious about the database structure, make a copy and explore it using the `sqlite3` tool. You can easily list all defined tables using the query below.

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




...jason's list
...productivity tools
