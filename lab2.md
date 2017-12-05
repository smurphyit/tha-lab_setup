#### Instructions
Now that you are comfortable with launching and shutting down your Kali VM feel free to familiarize yourself with the rest of our lab VMs:

**Vulnerable Client**

  ```
  vagrant up client
  ```

**Vulnerable Server**

  ```
  vagrant up web
  ```

**Network Emulator**

  ```
  vagrant up net
  ```

**Metasploitable**

  ```
  vagrant up metasploitable
  ```

##### Notes
  * The first time you issue the `vagrant up` command for a new VM you will be downloading a rather large file so be aware of the disk space requirements. 
  * Each of the VMs we offer are already configured to be networked together as required to complete our labs so understand that changing any network settings on the labs may break the functionality.

##### Deletion of VMs
  * To fully delete a virtual machine, you need to run `vagrant destroy [vmname]` in the directory with the THA Vagrantfile in it.
  
##### Managing VMs Downloaded from THA
  * The command `vagrant box list` and `vagrant box remove` can be used to show the local cache of VMs downloaded and to delete them from your local disk.

This concludes this block of instruction.
