# Unix Concepts


Concepts related to Unix


* Linux Network Namespaces (netns)
* VEth is a Virtual Ethernet device type
* Interruption Vector
Determines which routines provide service to certain interruptions/exceptions/system calls.

* In UNIX, it is possible to use the `NULL` virtual device to dump anything that we don't want to output anywhere else.

## System
* Check processor information
```bash
grep "model name" /proc/cpuinfo
```

* Get the 11 processes taking more system resources
```bash
ps h -eo pcpu,comm | sort -nr | head -11
```

* Get the total number of processes registered in the system
```bash
ps h -u root | wc -l
```

* List the users with registeres processes
```bash
ps h -ef | cut -f1 -d " " | sort | uniq
```

### D-Bus
In computing, D-Bus (short for "Desktop Bus") is a software bus, inter-process communication (IPC), and remote procedure call (RPC) mechanism that allows communication between multiple processes running concurrently on the same machine. D-Bus was developed as part of the freedesktop.org project, initiated by Havoc Pennington from Red Hat to standardize services provided by Linux desktop environments such as GNOME and KDE.

* init
In Unix-based computer operating systems, init (short for initialization) is the first process started during booting of the computer system. Init is a daemon process that continues running until the system is shut down. It is the direct or indirect ancestor of all other processes and automatically adopts all orphaned processes. Init is started by the kernel during the booting process; a kernel panic will occur if the kernel is unable to start it. Init is typically assigned process identifier 1.  

* runlevel
A runlevel is a mode of operation in the computer operating systems that implement Unix System V-style initialization. Conventionally, seven runlevels exist, numbered from zero to six. S is sometimes used as a synonym for one of the levels. Only one runlevel is executed on startup; run levels are not executed one after another (i.e. only runlevel 2, 3, or 4 is executed, not more of them sequentially or in any other order).  
A runlevel defines the state of the machine after boot. Different runlevels are typically assigned (not necessarily in any particular order) to the single-user mode, multi-user mode without network services started, multi-user mode with network services started, system shutdown, and system reboot system states. The exact setup of these configurations varies between operating systems and Linux distributions. For example, runlevel 4 might be a multi-user GUI no-server configuration on one distribution, and nothing on another. Runlevels commonly follow the general patterns described in this article; however, some distributions employ certain specific configurations. 

* [systemd](https://systemd.io/)
is an implementation of the init process in Unix, also a software suite that provides an array of system components for Linux operating systems.  
Its main aim is to unify service configuration and behavior across Linux distributions; systemd's primary component is a "system and service manager"—an init system used to bootstrap user space and manage user processes. It also provides replacements for various daemons and utilities, including device management, login management, network connection management, and event logging.  
The name systemd adheres to the Unix convention of naming daemons by appending the letter d. It also plays on the term "System D", which refers to a person's ability to adapt quickly and improvise to solve problems. 
systemctl is a program to control systemd.

* [systemd-homed](https://www.freedesktop.org/software/systemd/man/systemd-homed.service.html)
Run systemd as a user level process

* unit
A unit is a service in systemd