Title: /proc filesystem
Date: 2016-11-30 11:26

## System related

`/proc/cmdline`
kernel command line parameters/options

`/proc/cpuinfo`
CPU info

`/proc/devices`
list of major numbers and device groups

`/proc/diskstats`
disk I/O statistics for each disk device
see the Linux kernel source file Documentation/iostats.txt for more information

`/proc/filesystems`
list of filesystems supported by kernel

`/proc/interrupts`
number of interrupts per CPU per IO device

`/proc/loadavg`
load average figures, runnable and total processes and threads, last created PID

`/proc/locks`
current file locks and leases

`/proc/meminfo`
memory usage statistics

`/proc/mounts`
symlink to /proc/self/mounts

`/proc/net`
see netstat(8)

`/proc/partitions`
major and minor numbers of each partition

`/proc/stat`
kernel/system statistics

`/proc/uptime`
uptime and idle time


## Process related

`/proc/{PID}/cwd`
symlink to the current working directory of the process

`/proc/{PID}/environ`
process environment

`/proc/{PID}/exe
symlink to the actual pathname of the executed command

`/proc/{PID}/fd`
symlinks to open file descriptors

`/proc/{PID}/fdinfo`
iformation about opened files

`/proc/{PID}/io`
I/O statistics

`/proc/{PID}/limits`
resource limits

`/proc/{PID}/maps`
currently mapped memory regions and their access permissions
`/proc/{PID}/maps`
memory consumption

`/proc/{PID}/mem`
access to memory pages through open(2), read(2) and lseek(2)

`/proc/{PID}/mounts`
list of all the filesystems currently mounted in the mount namespace

`/proc/{PID}/root`
symbolic link that points to the root directory

`/proc/{PID}/status`
human readable process information

`/proc/{PID}/task`
directory contains one subdirectory for each thread
