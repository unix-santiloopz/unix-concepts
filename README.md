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