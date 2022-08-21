# Linux Server Administration 

## Course description:

This course delves into managing, automation techniques, best practices to ensure scalability, secure development and deployment of applications on a linux server.

#### Pre-requisites 

Basic working knowledge of linux and commands.

You can check out the [Intro to Linux](https://github.com/AdafroLabs/Intro-to-Linux-2022) course by adafrolabs incase you are totally new to it.

---

## Objectives

1. [Learn what servers are](#what-is-a-server)
2. [Look at the various types of servers](#types-of-servers)
3. [Deep dive into linux servers](#deep-dive-into-linux-servers)
4. [How to choose the right server?](#how-to-choose-the-right-server)
5. [Hypervisors of linux servers](#hypervisors-that-can-run-linux-servers)
6. [Best Security practices](#best-security-practices)
7. [Automation & Monitoring for server administration](#automation--monitoring-for-server-administration)
8. [Managing User accounts and Groups](#managing-user-accounts-and-groups)
9. [Server Network and Connectivity Configuration](#server-network-and-connectivity-configuration)

---
### What is a server?
A server sends, receives, and stores data. Fundamentally, it "serves" something else and is there to offer services.

### Types of Servers

        - Mail Server

        - Web Server

        - Proxy Server

        - File & Print Server

        - Database Server


### Deep dive into linux servers

- Installing and Configuring a Linux Server
    Steps:
    1. Download the ISO image of the linux distro you wish to install
    2. Mount the image onto the virtual machine if it is to set it up for one or insert the bootable flashdrive with the ISO image in the server hardware CPU unit or server unit.
    Alternative: Do a PXE boot with the image you have attained which is on the shared network with the server box you want to setup.
    3. Follow the steps stated to install the right logical volumes and groups , you may use  the defaults to start.You will need to specify a root password as a final step that you should keep very secret from unauthorised users
    4. Viola!! you have successfully installed and configured your linux server for use.

- Physical volumes, Volume groups and Logical Volumes
    - [guide](https://web.mit.edu/rhel-doc/5/RHEL-5-manual/Cluster_Logical_Volume_Manager/)

- *Daemon Processes / Services :*
    As stated in the definition of servers, they mainly exist to provide services. We tend to often label these as daemon processes. There are a couple of processes / services that have been open sourced and can easily be installed with a simple update or get command. 
    The most common services management software suite is [systemd](https://systemd.io/)
    With this you will often be able to use the `systemctl` command to check the enable, start, stop, and check the status of services . For more o the commands to use, check out this [man page](https://www.man7.org/linux/man-pages/man1/systemctl.1.html) 

    You may as well have custom made services that can easily be started and stopped using this software suite. It is important to ensure services are enabled such that on the reboot, they are able to start automatically.

- *Installing softwares and packages :*
    Different linux distributions have various ways in which one can install software and packages for example for the RHEL , fedora and centOS distros, the `yum` command and `dnf` command are often used for this purpose.

    The Ubuntu distro uses the `apt` command. 
    One thing to note is before you update or install any package, always ensure that the repositories collection command is always up to date. You can do this with a `yum update` or an `apt update` and `apt upgrade` command depending on the linux distro you are using.

- High Availability Clusters and resilient Storage

- *Upgrading Linux Servers :*
    Servers always need to be upgraded to the latest O.S version supported by the extended support license due to the constant security patches , robust features and design pattern changes the contributors make to them. In order to prevent your system server from being exploited by hackers , you will find yourself upgrading to newer supported OS versions. This can be done in a variety of ways as shown below

    - *Inplace upgrades :*
        You move from an older version of the operating system to a newer version, while staying on the same physical hardware. 
    - *Migration :* 
        You move from an older version of the operating system to a newer version of the operating system, by transferring to a different set of hardware or virtual machine.
    - *Cluster OS Rolling Upgrade.* You upgrade the operating system of your cluster nodes without stopping the Hyper-V or the Scale-Out File Server workloads. 
### How to choose the right server?


### Hypervisors that can run linux servers

-> What is a KVM Switch?

Kernel-based Virtual Machine (KVM) is an open source virtualization technology built into Linux. [ref](https://www.redhat.com/en/topics/virtualization/what-is-KVM)

Steps to set up a KVM [here](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/virtualization_deployment_and_administration_guide/sect-system_requirements-kvm_requirements)

### Best Security practices
    - [PAM Modules](https://www.redhat.com/sysadmin/pluggable-authentication-modules-pam)
    - ACL Access Control Lists

### Automation & Monitoring for server administration
    - Cron Jobs

-> Logrotate 

    - This allows you to easily administer various log files  
    - view man page

-> `top` command 

    - For cpu utilisation views on memory 

-> IaC(Infrastructure as Code)

This is the process of provisioning and managing infrastructure through code. In this way, you can deploy , manage and configure resources such as Virtual machines with lines of code.

    - tools
        * [Ansible](https://www.ansible.com/)
        * [Terraform](https://www.terraform.io/)
        * 

### Managing User accounts and Groups

The common commands that one will use as they manage various users and groups on a server are below

- Adding user

    ```bash
    $ useradd <user_name>
    ```

- Password change

    ```bash
    $ passwd <user_name>
    ```

- *Adding user to a group*

- *GECOS :*
This is a small description about the user that helps one identify them easily. In order to view a list of all users on a server, you need to be logged in as a sudoer and typt `cat /etc/passwd` The fields below will show

```
amark:x:1001:1001:mark,,,:/home/mark:/bin/bash
[--] - [--] [--] [-----] [--------] [--------]
|    |   |    |     |         |        |
|    |   |    |     |         |        +-> 7. Login shell
|    |   |    |     |         +----------> 6. Home directory
|    |   |    |     +--------------------> 5. GECOS
|    |   |    +--------------------------> 4. GID
|    |   +-------------------------------> 3. UID
|    +-----------------------------------> 2. Password
+----------------------------------------> 1. Username
```
In order to edit the finger details of a user, you can use the command below which should change the GECOS description

`chfn <user name> -f <user description>`

P.S user description has to be in quotes and can be e.g Application Administrator Account

You can use `finger username -l` to view the finger information

if finger is not installed use yum install finger to add it for CentOS, fedora and RHEL servers

### Server Network and Connectivity Configuration



---
## Lectures (Notes & Labs)

[Notes](https://github.com/AdafroLabs/Intro-to-Linux-Server-Admin/tree/main/Notes)

### Linux Server Admin

### Commonly used commands

---
### Linux servers

* openSUSE
* Ubuntu Server
* Oracle Linux
* CentOS
* Arch Linux
* Mageia
* ClearOS
* [RHEL](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/part-basic_system_configuration)
* Gentoo
* Fedora
* Fedora
* Megia

