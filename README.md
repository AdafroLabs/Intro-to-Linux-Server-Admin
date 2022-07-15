# Linux Server Administration 

## Course description:

This course delves into managing, automation techniques, best practices to ensure scalability, secure development and deployment of applications on a linux server.

#### Pre-requisites 

This course assumes basic knowledge of working with linux and basic linux commands.

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
A server stores, sends, and receives data. In essence, it "serves" something else and exists to provide services. 

### Types of Servers

        - Mail Server

        - Web Server

        - Proxy Server

        - File & Print Server

        - Database Server


### Deep dive into linux servers

- Installing and Configuring a Linux Server
- Physical volumes, Volume groups and Logical Volumes
    - [guide](https://web.mit.edu/rhel-doc/5/RHEL-5-manual/Cluster_Logical_Volume_Manager/)

- Daemon Processes
- Installing softwares and packages
- High Availability Clusters and resilient Storage
- Upgrading Linux Server
    
    -Inplace upgrades

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

- Adding user to a group


### Server Network and Connectivity Configuration



---
## Lectures (Notes & Labs)

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

