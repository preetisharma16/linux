
# CMPE283-Assignment-2
Its an individual assignment. All work is done by me: Priti Sharma(014561274)
Setting Up the Environment
1.	Running this assignment on Linux machine(400 GB hard disk space and 15 GB memory) with SVM virtualization features exposed
     and has AMD processor.
     
     run $ cat/proc/cpuinfo | more

     ![image 1](./temp/svm.png?raw=true )

2. verify processor support for KVM, output should be “kvm-ok” and “KVM acceleration can be used”.

![image 1](./temp/kvm.png?raw=true )

Building The Kernel 
1.	Open the terminal and clone this repository  https://github.com/torvalds/linux 
2.	run following commands in linux folder:
     sudo bash
    
     apt-get install build-essential kernel-package fakeroot libncurses5-dev libssl-dev ccache bison flex libelf-dev
     
     uname -a   (check your kernel version)
     
     its Linux 5.4.0-52-generic
    
    
    make a copy of config file into the current directory cp /boot/config-YOUR_KERNEL_VERSION ./.config
    
    make oldconfig (with all the default option by pressing enter key)
    
    build it make && make modules && make install && make modules_install
    
    reboot
    
    uname -a   (kernal version is updated)
    
    ![image 1](./temp/uname.png?raw=true )
