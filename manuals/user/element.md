---
layout: manual
title: User Manual
manual: user
manpage: element
category: manuals
---

# Elements

Elements are the central entities in your topology. They represent [end-hosts](device), [network infrastructure](switch), other elments' [network interfaces](interface), or connectors to [external networks](external_network).

## Element Types

There are different types of elements. Element functionality highly depends on the respective element type, and thus, each of them has its own manual page.

[TODO: image showing different element types]


* [*Network Interfaces*](interface) only exist with other elements and represent their network interfaces.
* [*Devices*](device) are end-hosts, usually realized as virtual machines. They can also be used to emulate network infrastructure.
* [*Switches*](switch) represent network infrastructure
* [*External networks*](external_network) are connectors to external networks.

{:.alert .alert-info}
This manual only covers subjects that apply to all elements. For further information, check the manual pages of the respective element type.

## Right-Click Menu

Most interactions with your elements is available in their respective right-click menus. To open it, point your mouse over the target element and press the right mouse button.

![right-click menu](../img/element-rightclick.png)

The right-click menu of an element usually contains the following functions:

* *Connect*: [Connect](#connection) elements
* [*Actions*](action)
* *Resource usage*: [Quota](../account#quota) Quota information
* *Disk image*: [Disk image](device/image) functions
* *Executable archive*: [Executable archive](device/executable_archive) functions
* *Configure*: Opens the element's configuration window.

## <a name="connection"></a>Connections Between Elements

You can create [network connections](../connection) between your elements.

{:.alert .alert-info}
As long as you have not explicitly connected elements to the Internet, there is no network connection between any element and the Internet.

When you create connections between elements, the topology editor will automatically create the respective [interface elements](interface).

{:.alert .alert-info}
You cannot create a connection when one of the to-be-connected elements is in the _started_ state.

## <a name="state"></a>States

Elements can be in different states. The state indicates the current status of deployment on a host

[TODO: image showing different element states]

The states are:

* *created*: The element is created in the editor, but not deployed on any host yet.
* *prepared*: The element is deployed on a host, but not running (i.e., the virtual machine is stopped).
* *started*: The element is deployed on a host and running.

{:.alert .alert-info}
Some types of elements do not support the _started_ state.

To change the state of an element, you have to run the specific [actions](action).

The available element functionality highly depends on its state.


## Configuration Window

Every element has a configuration window which can be accessed via its right-click menu. Please refer to the respective element type's manual page for more information about configuration options.


## Access to Your Elements

Almost all functions to access your elements are available from their right-click menu. See the respective element type for more details.

