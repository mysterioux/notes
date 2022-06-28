# Curriculum with Edx

C1: 	The Linux Foundation [done]
C2: 	Linux Philosophy and Concepts 
C3: 	Linux Basics and System Startup
C4: 	Graphical Interface
C5: 	System Configuration from the Graphical Interface
C6: 	Common Applications
C7:		Command Line Operations
C8: 	Finding Linux Documentation
C9: 	Process
C10:	File Operations
C11: 	Text Editors
C12:	User Environment
C13:	Manipulating Text
C14:	Network Operations
C15:	The Bash Shell and Basic Scripting
C16:	More on Bash Shell Scripting
C17:	Printing
C18:	Local Security Principles

### Sources:
- https://training.linuxfoundation.org/
- https://training.linuxfoundation.org/full-catalog/?_sft_product_type=training
- https://events.linuxfoundation.org/
- https://devswag.io/

---
Lesson 1 : The Linux Foundation
---

Learning Objectives: By the end of this chapter, you should be able to:

* Discuss the role of The Linux Foundation.
* Appreciate the learning opportunities provided by The Linux Foundation's training program.
* Describe the software environment required for this course.
* Describe the three major Linux distribution families.

Linux foundation was founded in 2002. Linux Foundation is home to its creator Linux Torvalds and lead maintainer Greg Kroah-Hartman. LF is a vendor-netural, non-profit organization dedicated to supporting the open source community through financial and intellectual resources, infratructural services, events and training.

There are 3 Major Distribution Family
1. Red Hat Family Systems [Including CentOS and Fedora]
2. SUSE Family Systems [including openSUSE]
3. Debian Family Systems [including Ubunut and Linux Mint]

The Structure of Linux Distros:

						Linux Kernel
							 |
							 V
			--------------------------------------------> Other Distributions
			  |			   |					|
			Debian		  RHEL		   		   SUSE
			  |			   |					|
			Ubuntu		 Fedora				   SLES
			  |			 /	\					|
		 Linux Mint   	/	 \				 openSUSE
		 			CentOS   Oracle Linux
ref: https://lwn.net/Distributions/

### The Red Hat Family
Red Hat Enterprise Linux (RHEL) heads the family that includes CentOS, CentOS Stream, Fedora and Oracle Linux.
Note: 
- Fedora has a close relationhip to RHEL thus it is been used as a upstream updates for RHEL. 
- CentOS Stream gets updated ahead of RHEL while CentOS gets updated after RHEL. 
- CentOS is a close clone of RHEL. 
- A heavily patched version 3.10 Kernel is used in RHEL/CentOS 7, while version 4.18 is used in RHEL/CentOS 8.
- It uses the `yum` and `dnf` RPM-based yum package managers to install, update and remove packages in the system.
- RHEL is widely used in enterprise that host their own systems.


### The SUSE Family
The relationship between SUSE  (SUSE Linux Enterprise Server, or SLES) and openSUSE is similar to the one described between RHEL, CentOS, and Fedora. openSUSE can be used as the reference distribution for the SUSE family, as it is available to end users at no cost.
Note:
- SUSE Linux Enterprise Server (SLES) is upstream for openSUSE
- Kernel version 4.12 is used in openSUSE Leap 15
- SLES is widely used in retail and many other sectors
- It includes the YaST (Yet Another Setup Tool) application for system administration purposes
- It uses the RPM-based zypper package manager to install, update and remove packages in the system.


### The DEBIAN Family
The Debian distribution is upstream for several other distributions, including Ubuntu. In turn, Ubuntu is upstream for Linux Mint and a number of other distributions. It is commonly used on both servers and desktop computers. Debian is a pure open source community project (not owned by any corporation) and has a strong focus on stability. 
Note:
- Debian provides by far the largest and most complete software repository to its users of any Linux distribution.
- The Debian family is upstream for Ubuntu and in return Ubuntu is upstream for other platforms like Linux Mint.
- Kernel version 5.8 is used in Ubuntu 20.04 LTS
- It uses the DPKG-based APT package manager (using apt, apt-get, apt-cache,etc) to install, update and remove packages in the system
_ Even though it is built on top of Debian, it uses GNOME-based under the hood.


Note: Most distributions differe on the use of their package management systems, software versions and file locations. This is why linux skills can be migrated swiftly across different distros.

---
Lesson 2 : Linux Philosophy and Concepts
---
Learning Objectives: By the end of this chapter, you should be able to:

* Discuss the history and philosophy of Linux.
* Describe the Linux community.
* Define the common terms associated with Linux.
* Discuss the components of a Linux distribution.

Linux is an open source computer operating system, initially developed on and for Intel x86-based personal computers. It has been subsequently ported to an astoundingly long list of other hardware platforms, from tiny embedded appliances to the world's largest supercomputers.

Linus Torvalds was a student in Helsinki, Finland, in 1991, when he started a project: writing his own operating system kernel. 

Linux is a fully multitasking (i.e. multiple threads of execution are performed simultaneously), multiuser operating system, with built-in networking and service processes known as daemons in the UNIX world.

Linux borrows heavily from the well-established UNIX operating system. It was written to be a free and open source system to be used in place of UNIX, which at the time was designed for computers much more powerful than PCs and was quite expensive.

NOTE: Linux was inspired by UNIX, but it is not UNIX.

The Linux community is a far-reaching ecosystem consisting of developers, system administrators, users and vendors who use many different forums to connect with one another.

### Linux Terminology
-> Kernel : The brain of the operating system that glue between hardward and applications.

-> Distributors : A collection of software combined with the linux kernel making up a linux-based OS (e.g Ubuntu, Fedora)

-> Boot loader: A program that boots the operating system (GRUB / ISOLINUX)

-> Service: A program that runs as a background process (httpd, nfsd, ntpd, ftpd etc)

-> Filesystem:  A method of storing and organizing files in linux (e.g ext3, ext4, FAT, XFS, NTFS, Btrfs)

-> X Window System: provides standard tool kits and protocol for building graphical user interface on nearly all linux systems.

-> Desktop Environment: GUI on top of the operating system (GNOME, KDE, Xfce, Fluxbox)

-> Command Line: An interface for typing commands on top of the operating system. The Shell -> is the command line interpreter that interprets the command line input and instructs the operating system to perform any necessary tasks and commands. (bash, tch, zsh)

A Distribution (RHEL,Ubuntu,Debian etc) has:

	-Linux Kernel
		|__ Applications
		|__ Package Updates, Upgrades kernel and driver patches
		|__ Libraries, Utilities, Configuration
		|__ Support Services:Commercial/Community
		|__ Documentation for: Commands, Application,Services


---
Lesson 3 : Linux Basics and System Startup
---

Learning Objectives: By the end of this chapter, you should be able to:

* Identify Linux filesystems.
* Identify the differences between partitions and filesystems.
* Describe the boot process.
* Install Linux on a computer.


## The Boot Process
The Linux boot process is the procedure for initializing the system. It consists of everything that happens from when the computer power is first switched on until the user interface is fully operational. 

The process is as follow:

			
	    Power On
		|
		v
	      BIOS
	  	|
	  	v
	Master Boot Record (MBR) also know as First Secotr of the Hard Disk
		|
		v
	Boot Loader (e.g GRUB OR ISOLINUX)
		|
		v
	Kernel (Linux OS)
		|
		v
	Inital RAM disk- initramfs image
		|
		v
	/sbin/init (parent process)
		|
		v
	Command Shell using getty
		|
		v
	X Windows System (GUI - e.g GNOME, Xfce)


## The Boot Process
When the computer is powered on, the Basic Input/Output System (BIOS) initializes the hardware, including the screen and keyboard, and tests the main memory. This process is also called POST (Power On Self Test).

	Power On
	|
	v
	BIOS (Basic Input/Output System)
	|
	v
	Initializes the screen and keyboard and test the main memory

The BIOS software is stored on a ROM chip on the motherboard. After this, the remainder of the boot process is controlled by the operating system (OS).

## Master Boot Record (MBR) and Boot Loader
Once the POST is completed, the system control passes from the BIOS to the boot loader. The boot loader is usually stored on one of the hard disks in the system, either in the boot sector (for traditional BIOS/MBR systems) or the EFI partition (for more recent (Unified) Extensible Firmware Interface or EFI/UEFI systems). Up to this stage, the machine does not access any mass storage media. Thereafter, information on date, time, and the most important peripherals are loaded from the CMOS values (after a technology used for the battery-powered memory store which allows the system to keep track of the date and time even when it is powered off).

A number of boot loaders exist for Linux; the most common ones are GRUB (for GRand Unified Boot loader), ISOLINUX (for booting from removable media), and DAS U-Boot (for booting on embedded devices/appliances). Most Linux boot loaders can present a user interface for choosing alternative options for booting Linux, and even other operating systems that might be installed. When booting Linux, the boot loader is responsible for loading the kernel image and the initial RAM disk or filesystem (which contains some critical files and device drivers needed to start the system) into memory.

## Boot Loader in Action

The boot loader has two distinct stages:

For systems using the BIOS/MBR method, the boot loader resides at the first sector of the hard disk, also known as the Master Boot Record (MBR). The size of the MBR is just 512 bytes. In this stage, the boot loader examines the partition table and finds a bootable partition. Once it finds a bootable partition, it then searches for the second stage boot loader, for example GRUB, and loads it into RAM (Random Access Memory). For systems using the EFI/UEFI method, UEFI firmware reads its Boot Manager data to determine which UEFI application is to be launched and from where (i.e. from which disk and partition the EFI partition can be found). The firmware then launches the UEFI application, for example GRUB, as defined in the boot entry in the firmware's boot manager. This procedure is more complicated, but more versatile than the older MBR methods.

The second stage boot loader resides under [/boot]. A splash screen is displayed, which allows us to choose which operating system (OS) to boot. After choosing the OS, the boot loader loads the kernel of the selected operating system into RAM and passes control to it. Kernels are almost always compressed, so its first job is to uncompress itself. After this, it will check and analyze the system hardware and initialize any hardware device drivers built into the kernel.

## Initial RAM Disk
The initramfs filesystem image contains programs and binary files that perform all actions needed to mount the proper root filesystem, like providing kernel functionality for the needed filesystem and device drivers for mass storage controllers with a facility called udev (for user device), which is responsible for figuring out which devices are present, locating the device drivers they need to operate properly, and loading them. After the root filesystem has been found, it is checked for errors and mounted.

The initramfs filesystem image contains programs and binary files that perform all actions needed to mount the proper root filesystem, like providing kernel functionality for the needed filesystem and device drivers for mass storage controllers with a facility called udev (for user device), which is responsible for figuring out which devices are present, locating the device drivers they need to operate properly, and loading them. After the root filesystem has been found, it is checked for errors and mounted.

The mount program instructs the operating system that a filesystem is ready for use, and associates it with a particular point in the overall hierarchy of the filesystem (the mount point). If this is successful, the initramfs is cleared from RAM and the init program on the root filesystem (/sbin/init) is executed.

init handles the mounting and pivoting over to the final real root filesystem. If special hardware drivers are needed before the mass storage can be accessed, they must be in the initramfs image.

## Text-Mode Login
Near the end of the boot process, init starts a number of text-mode login prompts. These enable you to type your username, followed by your password, and to eventually get a command shell. However, if you are running a system with a graphical login interface, you will not see these at first.

As you will learn in Chapter 7: Command Line Operations, the terminals which run the command shells can be accessed using the ALT key plus a function key. Most distributions start six text terminals and one graphics terminal starting with F1 or F2. Within a graphical environment, switching to a text console requires pressing CTRL-ALT + the appropriate function key (with F7 or F1 leading to the GUI).

Usually, the default command shell is bash (the GNU Bourne Again Shell), but there are a number of other advanced command shells available. The shell prints a text prompt, indicating it is ready to accept commands; after the user types the command and presses Enter, the command is executed, and another prompt is displayed after the command is done.

## The Linux Kernel
The boot loader loads both the kernel and an initial RAM–based file system (initramfs) into memory, so it can be used directly by the kernel.

When the kernel is loaded in RAM, it immediately initializes and configures the computer’s memory and also configures all the hardware attached to the system. This includes all processors, I/O subsystems, storage devices, etc. The kernel also loads some necessary user space applications.

## /sbin/init and Services
Once the kernel has set up all its hardware and mounted the root filesystem, the kernel runs /sbin/init. This then becomes the initial process, which then starts other processes to get the system running. Most other processes on the system trace their origin ultimately to init; exceptions include the so-called kernel processes. These are started by the kernel directly, and their job is to manage internal operating system details.

Besides starting the system, init is responsible for keeping the system running and for shutting it down cleanly. One of its responsibilities is to act when necessary as a manager for all non-kernel processes; it cleans up after them upon completion, and restarts user login services as needed when users log in and out, and does the same for other background system services.

## Startup Alternatives
SysVinit viewed things as a serial process, divided into a series of sequential stages. Each stage required completion before the next could proceed. Thus, startup did not easily take advantage of the parallel processing that could be done on multiple processors or cores.

The two main alternatives developed were:

* Upstart
- Developed by Ubuntu and first included in 2006
- Adopted in Fedora 9 (in 2008) and in RHEL 6 and its clones

* systemd
- Adopted by Fedora first (in 2011)
- Adopted by RHEL 7 and SUSE 
- Replaced Upstart in Ubuntu 16.04


## systemd Features
Systems with systemd start up faster than those with earlier init methods. This is largely because it replaces a serialized set of steps with aggressive parallelization techniques, which permits multiple services to be initiated simultaneously.

One thing to note is that [/sbin/init] now just points to [/lib/systemd/systemd]; i.e. systemd takes over the init process.

One systemd command (systemctl) is used for most basic tasks. While we have not yet talked about working at the command line, here is a brief listing of its use:

Starting, stopping, restarting a service (using httpd, the Apache web server, as an example) on a currently running system:

```bash
$ sudo systemctl |start|stop|restart httpd.service
# Enabling or disabling a system service from starting up at system boot:
$ sudo systemctl |enable|disable httpd.service
```
In most cases, the .service can be omitted. There are many technical differences with older methods that lie beyond the scope of our discussion.  

 ## Linux Filesystems
The Linux filesystem, which is the embodiment of a method of storing and organizing arbitrary collections of data in a human-usable form.

Different types of filesystems supported by Linux:

* Conventional disk filesystems: [ext3, ext4, XFS, Btrfs, JFS, NTFS, vfat, exfat, etc.]
* Flash storage filesystems: [ubifs, jffs2, yaffs, etc.]
* Database filesystems
* Special purpose filesystems: [procfs, sysfs, tmpfs, squashfs, debugfs, fuse, etc].

## Partitions and Filesystems
A partition is a physically contiguous section of a disk, or what appears to be so in some advanced setups.

A filesystem is a method of storing/finding files on a hard disk (usually in a partition). 

One can think of a partition as a container in which a filesystem resides, although in some circumstances, a filesystem can span more than one partition if one uses symbolic links, which we will discuss much later.

|		  		| windows	| 		Linux |
|---------------|-----------|-------------|
|Partition 		| Disk 		| /dev/sda1   |
|Filessytem Type | NFTS/VFAT | EXT3/EXT4/XFS..|
|Mounting Paramenters | DriveLetter | MountPoint|
|Base Folder (where OS is stored)| C:\	| / |
