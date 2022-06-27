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