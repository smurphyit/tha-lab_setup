Hacker Academy
==============
http://hackeracademy.com

### THA LAB SETUP

#### Purpose
This lab will walk you through the steps required to set up the local testing environment required to complete the labs found at hackeracademy.com

#### Requirements
This lab requires the following software and hardware:
* One of the following: Virtualbox 4.3+,  VMWare Fusion 5.x+, VMWare Workstation 9+ 
* Vagrant
* Dual core CPU or better
* 3GB of RAM, 4GB+ recommended
* 60GB of storage space, SSD recommended

#### Setup
The THA lab environment supports Virtualbox and VMware Fusion/Workstation has been tested with Windows, OS X, and Linux hosts.

##### NOTE
*While using Virtualbox with Vagrant is free, using VMware Fusion or Workstation with Vagrant requires the purchase of a plugin from the developers of Vagrant. Available [here](https://www.vagrantup.com/vmware).
The following steps assume that you are either using Virtualbox or have purchased and installed the VMware plugin from Hashicorp.*

1. Download and install Vagrant from [here](https://www.vagrantup.com/downloads.html).
  * Be sure to install Vagrant version 1.7.2 or newer to avoid any issues.

2. Download and install Virtualbox if you haven't already done so. [Virtualbox.org](https://www.virtualbox.org/wiki/Downloads)
  * If you are using VMware then you do NOT need to install Virtualbox and can skip this step.

3. Right click the THA [Vagrantfile](https://raw.githubusercontent.com/madsec/tha-lab_setup/master/assets/Vagrantfile) and `save as` with the name `Vagrantfile` without any file extension. 
  * Windows may try to add the .sdx extension to the Vagrantfile, if it does simply remove the extension.
  * Failure to name the Vagrantfile properly (with no extension) will prevent your VMs from working.

4. Open a terminal and make sure you're in the same directory as the Vagrantfile, then launch your Kali VM by entering the following command:

  ```bash
  vagrant up kali
  ```

  * If you are using vmware and the vmware vagrant plugin, you may need to run `vagrant up kali --provider=vmware_fusion` or `vagrant up --provider=vmware_workstation` instead

5. The first time you run the `vagrant up` command it will download the Kali VM (wich can be quite large) and launch it via Virtualbox.
  * In Windows the VM image is typically stored in the users home directory.
  * In Linux/OSX the VM image is stored in `~/.vagrant.d`.

6. Inside your Kali VM, open a new terminal and issue the following commands to create a directory to hold the THA lab information and to clone this repository into it:

    ```bash
    git clone git://github.com/madsec/tha-lab_setup /root/THA/setup
    ```

##### Note
* If the Kali VM network connection continually disconnects, simply reboot the VM.

#### Start the lab
* Use the `Leafpad` application to open and follow the instructions for lab 1 found on your Kali machine at 
  ```
  /root/THA/setup/lab1.md
  ```
