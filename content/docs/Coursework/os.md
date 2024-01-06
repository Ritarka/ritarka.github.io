---
title: Systems
---

# Systems

I took two courses on systems, CS 3210 (Operating Systems) and CS 4210 (Advanced Operating Systems). In the former we went deep into the design of operating systems, but in the latter we took a larger view and tackled computer systems in general.

In OS the projects involved with a Unix like OS called [xv6](https://pdos.csail.mit.edu/6.828/2012/xv6.html): a unix inspired OS created by MIT for teaching.

The projects involved modifying xv6 to add some feature like:
1. A backtrace function
2. Copy-On-Write
3. Round Robin and FIFO scheduler
4. Kernel Threading
5. File Permissions and syscalls for chown and chmod
6. Login System

During AOS we covered everything from virtualization to distributed systems. Some noteable projects included building a load-balancer and memory coordinator to manage several virtual machine, as well as creating a weaker version of [map-reduce](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf).