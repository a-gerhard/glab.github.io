---
layout: default
title: Node Requirements
category: join
---

# Node Requirements

Each ToMaTo node must meet some minimum requirements to be usable for the platform.

## Node Hardware

* Multiple cores with **at least 2 GHz**
* x86 architecture with 64 bit support
* Support for **hardware virtualization** in the CPU
  - This means that the node must be physical and not a VM
  - You can check this requirement by executing:
    ``grep -qE 'flags.*(vmx|svm)' /proc/cpuinfo && echo "supported" || echo "not supported"``
* At least **12 GB RAM**
* At least **300 GB hard disk**

## Node connectivity

* At least 1 **GBit LAN** (site internally)
* Unfiltered access to the Internet
* At least one dedicated **public IPv4 address**

## Site requirements

* At least 1 MBit WAN (Internet access)

## Availability

* Planned availability of **at least 95% uptime**
* Technical support with reaction time within 3 work days

## Node Software

The nodes need to run a Debian based operating system with some additional packages installed for ToMaTo.

The [Proxmox VE virtualization](http://www.proxmox.com/proxmox-ve) system is fully supported by ToMaTo and currently is the recommended host operating system.
Using Proxmox as a base system has the advantage that additional virtual machines can be created and used besides ToMato.

The documentation explains the [installation procedure](https://tomato.readthedocs.org/en/latest/hostmanager/tomato/installation/). The administrators can assist with the installation if help is needed.
