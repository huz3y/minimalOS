Minimal OS
==========

Here we define what is the very barebones of a operating system.

The intention here, is not to define a source base that we will use in
the rest of the course, but instead to provide an overview of how to
actually get the very basics running, i.e booting your own kernel
within a virutal machine.

Our goal is the take the machine at its most basic, infact computers
really can't do very much without our instruction, and given this
starting point run a program, the operating system, to have it do
something useful.

Build
============

To build the minimal OS simply type:

    make

This will create the operating system binary itself:

    minimalos.bin


Run
  
    qemu-system-i386 --kernel minimal.bin
============

Now we have built our minimal OS we would like to run it. To do this
we could create a bootable CD and run it just like you would an OS
like Windows or Linux, however, its a pain to have to reboot our
machine all the time and so instead we can use a VM. You can now
load the IOS image into your choice of VM, I, for example, use
VMWare Fusion on my Mac, or for ease of use we can use 

    (QEMU)[wiki.qemu.org/Main_Page]

which is a an open source machine emulator and virtualizer. It should be
installed on the Linux machines for your labs and is straightfoward
to configure for a home Linux install. Once installed you can simply
run the ISO image with the command:

    qemu-system-i386 -cdrom minimalos.iso

What's going on under the hood with our minimal OS?
===================================================
