Title: /proc filesystem
Date: 2016-11-30 11:26

## System related

`cat /proc/cmdline`
kernel command line parameters/options

`cat /proc/cpuinfo`
CPU info

`cat /proc/devices`
list of major numbers and device groups

`cat /proc/diskstats`
disk I/O statistics for each disk device
see the Linux kernel source file Documentation/iostats.txt for more information

`cat /proc/filesystems`
list of filesystems supported by kernel

`cat /proc/interrupts`
number of interrupts per CPU per IO device

`cat /proc/loadavg`
load average figures, runnable and total processes and threads, last created PID

`cat /proc/locks`
current file locks and leases

`cat /proc/meminfo`
memory usage statistics

`ls /proc/mounts`
symlink to /proc/self/mounts

`cat /proc/net`
see netstat(8)

`cat /proc/partitions`
major and minor numbers of each partition

`cat /proc/stat`
kernel/system statistics

`cat /proc/uptime`
uptime and idle time


## Process related

`strings /proc/{PID}/environ`
process environment

`ls /proc/{PID}/fd`
open file descriptors

`ls /proc/{PID}/fdinfo`
iformation about opened files

`cat /proc/{PID}/io`
I/O statistics

`cat /proc/{PID}/limits`
resource limits

`cat /proc/{PID}/maps`
currently mapped memory regions and their access permissions
`cat /proc/{PID}/maps`
memory consumption

`/proc/{PID}/mem`
access to memory pages through open(2), read(2) and lseek(2)

`cat /proc/{PID}/mounts`
list of all the filesystems currently mounted in the mount namespace

`ls /proc/{PID}/root`
symbolic link that points to the root directory

`cat /proc/{PID}/status`
human readable process information

`ls /proc/{PID}/task`
directory contains one subdirectory for each thread
