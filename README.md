# CMPE 283: Virtualization Technologies
## Assignment 1: Discovering VMX Features 
###### Manikanta Nynala 

## Contribution of Manikanta Nynala:
Created the environment using VMware Fusion Pro and built kernel code for IA32_VMX_PROCBASED_CTLS  and IA32_VMX_PROCBASED_CTLS processor-based controls.

Created the environment using VMware Fusion Pro and built kernel code for IA32_VMX_ENTRY_CTLS and IA32_VMX_EXIT_CTLS  processor-based controls.

## Environment Setup

1. Download VMware Fusion Pro.

2. Create an outer virtual machine (VM) by selecting Ubuntu 64-bit as the guest operating system using the provided ISO image file.

3. Configure the outer VM with a 200 GB hard disk space and 4 GB of memory.

4. Run the VM and proceed with the Ubuntu installation.

5. Enable nested virtualization by adjusting the processor settings in the VMware Fusion for the outer VM.

6. Install KVM packages using the following commands and verify processor support for KVM:
   $ sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virt-manager
   $ ls -l /dev/kvm

7.  Install virt-manager with the command:
    $ sudo apt-get install virt-manager

8. Create an inner VM using the Virtual Machine Manager GUI, allocating 20 GB of hard disk space, and install Ubuntu within the inner VM.

9. Check if nested virtualization is enabled by executing the following command:
   $ cat /proc/cpuinfo | more

 ## Build and Development Process

1. Download the cmpe283-1.c and Makefile from the Canvas file section.
   
2. Installed make and GCC using the below commands.
    > $ sudo apt install make
    > $ sudo apt install gcc
    
3. Build the file using the Make command.
   
4. After building the make file, check if kernel object cmpe283-1.ko is created.


5. Loaded the kernel code for all the MSR’s (refer cmpe283-1.c).
6. Executed the below command to run the kernel 
7. To view the system log, executed the below command.
   $ dmesg

   ![Screenshot-1](https://github.com/manikantanynala97/CMPE283-Assignment1/assets/90610801/a0999b06-7e2b-4eb5-858a-fa4399c9526b)
   
   ![Screenshot-2](https://github.com/manikantanynala97/CMPE283-Assignment1/assets/90610801/6dad7166-0642-43c7-8837-cf3acd0e3b57)

   ![Screenshot-3](https://github.com/manikantanynala97/CMPE283-Assignment1/assets/90610801/d653d6d4-0295-4a89-a584-ad250a675f50)

   ![Screenshot-4](https://github.com/manikantanynala97/CMPE283-Assignment1/assets/90610801/01a2bff9-1b47-4152-ac88-6136814820ff)




