#### # Sort 
```bash
$ sort [option] filename.txt

$ cat file.txt
aa 2 tttt
bb 1 tttt
zz 10 ttt
bb 0 tttt
nn 100 ttt

$ sort -k 2 file.txt
bb 0 tttt
bb 1 tttt
zz 10 ttt
nn 100 ttt
aa 2 tttt

$ sort -k 2 -n file.txt
bb 0 tttt
bb 1 tttt
aa 2 tttt
zz 10 ttt
nn 100 ttt

$ sort -k 2 -n -r file.txt
nn 100 ttt
zz 10 ttt
aa 2 tttt
bb 1 tttt
bb 0 tttt
```
![sort](https://ping-t.com/mondai3/img/jpg/k33873.jpg)

#### # vi / vim 
![tune2fs](https://ping-t.com/mondai3/img/jpg/k33911.jpg)

#### # Telinit
```bash
telinit 0 
Power-off the machine. 
systemctl poweroff
shutdown -h now

telinit 6
Reboot the machine. 
systemctl reboot
shutdown -r now
reboot
```

#### # Filesystem
1. tune2fs - adjust tunable filesystem parameters on ext2/ext3/ext4 filesystems
```bash
$ tune2fs [option] DeviceName
$ tune2fs -L /WORK /dev/hda5
```
![tune2fs](https://ping-t.com/mondai3/img/jpg/k34080.jpg)

#### # Filesystem Hierarchy Standard
![FHS](https://ping-t.com/mondai3/img/jpg/k34123.jpg)

#### # fstab
```bash
# /etc/fstab
user: mount by everone, unmount by only one user
users: mount by everyone, unmount by everyone
nouser: no user can mount 
ro: read only
rw: read write
suid: suid and sgid available
```
![fstab](https://ping-t.com/mondai3/img/jpg/k34089.jpg)

```bash
# du
-a      Display an entry for each file in a file hierarchy.
-c      Display a grand total.
-h      "Human-readable" output.
-s      Display total for specified file/directory.

$ du -a dir
5144 dir/subdir1/test.txt
5148 dir/subdir1
5144 dir/subdir2/file
5148 dir/subdir2
4 dir/file1.txt
10304 dir

$ du -s dir
10304 dir

$ du -ch dir
5148 dir/subdir1
5148 dir/subdir2
10304 dir
10304 Total 
```

#### # Regular Expression
![Regular Expression](https://ping-t.com/mondai3/img/jpg/k34024.jpg)

#### # nice - run a program with modified scheduling priority
```
$ nice [-n niceValue] command
```
![nice value](https://ping-t.com/mondai3/img/jpg/k34014.jpg)

#### * Archive (zip, bz2, tar, gzip) -> [reference](https://jadi.gitbooks.io/lpic1/content/1033_perform_basic_file_management.html)
- tar 
```bash
# Compress and decompress tar.bzip2
$ tar cfjv test.tar.bzip2 /test
$ tar tfjv test.tar.bzip2
$ tar xfjv test.tar.bzip2

# Decompress test.tar.gz
$ tar xvfz test.tar.gz
$ tar xfz test.tar.gz
```
![tar-command-option](https://ping-t.com/mondai3/img/jpg/k33965.jpg)

- bz2 - How to unzip file.bz2?</br>
<b>Notes:</b> bzip2 only works with file
```bash
$ bunzip2 file.bz2
$ bzip2 -d file.bz2

# How to make file.bz2
$ bzip2 file.txt
-> file.txt.bz2 is created
```

#### # Devices
- USB device
```bash
$ lsusb
Bus 002 Device 002: ID 8087:0020 Intel Corp. Integrated Rate Matching Hub
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 002: ID 8087:0020 Intel Corp. Integrated Rate Matching Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

$ cat /proc/bus/usb/devices
...
```

#### # Package
1. apt-get
```bash
$ apt-get remove [package-name]
```
![apt-get](https://ping-t.com/mondai3/img/jpg/k33777.jpg)

2. rpm - RPM Package Manager
```bash
$ rpm --query --list postfix
$ rpm -ql posftfix
```
query<br>
![rpm](https://ping-t.com/mondai3/img/jpg/k33797.jpg)
install<br>
![rpm-install](https://ping-t.com/mondai3/img/jpg/k33792.jpg)

3. zypper - SUSE based package manager

4. yum
```bash
Command is one of:
    * install package1 [package2] [...]
    * update [package1] [package2] [...]
    * update-to [package1] [package2] [...]
    * update-minimal [package1] [package2] [...]
    * check-update
    * upgrade [package1] [package2] [...]
    * upgrade-to [package1] [package2] [...]
    * distribution-synchronization [package1] [package2] [...]
    * remove | erase package1 [package2] [...]
    * autoremove [package1] [...]
    * list [...]
    * info [...]
    * provides | whatprovides feature1 [feature2] [...]
    * clean [ packages | metadata | expire-cache | rpmdb | plugins | all ]
    * makecache [fast]
    * groups [...]
    * search string1 [string2] [...]
    * shell [filename]
```

#### # xargs - build and execute command lines from standard input 
```bash
$ cat file1.txt
aaaa.txt
bbbb.txt
cccc.txt

$ cat file1.txt | xargs touch

$ ls -l
total 4
-rw-r--r-- 1 root root  0 Apr 16 21:59 aaaa.txt
-rw-r--r-- 1 root root  0 Apr 16 21:59 bbbb.txt
-rw-r--r-- 1 root root  0 Apr 16 21:59 cccc.txt
-rw-r--r-- 1 root root 28 Apr 16 21:58 file1.txt
```

#### # Text Editing (sed)
1. sed - stream editor for filtering and transforming text
```bash
$ sed -e s/pingt/hoge/g test.txt
$ sed s/pingt/hoge/g test.txt 
```
![sed](https://ping-t.com/mondai3/img/jpg/k34032.jpg)

2. tr - Translate, squeeze, and/or delete characters from standard input, writing to standard output.
```bash
$ cat file
aaa BBB
111 222
abc 123 ab3

$ cat file | tr -s [:lower:]
a BBB
111 222
abc 123 ab3

$ cat file.txt
PINGT
PINGT

$ cat file.txt | tr PINGT pingt
pingt 
pingt
```
![tr-option](https://ping-t.com/mondai3/img/jpg/kk33884.jpg)
![tr-option2](https://ping-t.com/mondai3/img/jpg/kkk33884.jpg)

3. Line number
- cat
```bash
$ cat file.txt
aaa
bbb

ccc
ddd

eee

$ cat -n file.txt
     1  aaa
     2  bbb
     3
     4  ccc
     5  ddd
     6
     7  eee

$ cat -b file.txt
     1  aaa
     2  bbb

     3  ccc
     4  ddd

     5  eee
     
$ nl file.txt
     1  aaa
     2  bbb

     3  ccc
     4  ddd

     5  eee
```


#### # Process
1. ps - report a snapshot of the current processes.
```bash
# To see every process on the system using standard syntax:
$ ps -ef 
UID        PID  PPID  C STIME TTY          TIME CMD
root         1     0  0 Apr15 ?        00:00:12 /usr/lib/systemd/systemd 
root         2     0  0 Apr15 ?        00:00:00 [kthreadd]
root         3     2  0 Apr15 ?        00:00:00 [ksoftirqd/0]

# To see every process on the system using BSD syntax:
$ ps ax
PID TTY      STAT   TIME COMMAND
    1 ?        Ss     0:12 /usr/lib/systemd/systemd 
    2 ?        S      0:00 [kthreadd]
    3 ?        S      0:00 [ksoftirqd/0]
```
![ps-process](https://ping-t.com/mondai3/img/jpg/k34339.jpg)

#### # history
```bash
$ echo $HISTFILE
/root/.bash_history

$ echo $HISTSIZE
1000

$ history
```

#### # RunLevel
```bash
$ runlevel
N 5
```
![RunLevel](https://ping-t.com/mondai3/img/jpg/k33726.jpg)

#### # Hard Disk Design
- Physical Volume (pv): a whole drive or a partition. It is better to define partitions and not use whole disks - unpartitioned.
- Volume Groups (vg): this is the collection of one or more pvs. OS will see the vg as one big disk. PVs in one vg, can have different sizes or even be on different physical disks.
- Logical Volumes (lv): OS will see lvs as partitions. You can format an lv wit your OS and use it.
![pv-vg-lv](https://ping-t.com/mondai3/img/jpg/k34230.jpg)

- fdisk is the main command for viewing / changing and creating<br>
```bash
Command (m for help): m
Command action
   a   toggle a bootable flag
   b   edit bsd disklabel
   c   toggle the dos compatibility flag
   d   delete a partition
   g   create a new empty GPT partition table
   G   create an IRIX (SGI) partition table
   l   list known partition types
   m   print this menu
   n   add a new partition
   o   create a new empty DOS partition table
   p   print the partition table
   q   quit without saving changes
   s   create a new empty Sun disklabel
   t   change a partition's system id
   u   change display/entry units
   v   verify the partition table
   w   write table to disk and exit
   x   extra functionality (experts only)
```

- <b>Primary, Extended & Logical Partitions</b>
<p>The partition table is located in the master boot record (MBR) of a disk. The MBR is the first sector on the disk, so the partition table is not a very large part of it. This limits the primary partitions to 4 and the max size of a disk to around 2TBs. If you need more partitions you have a define one extended and then create logicals inside them.</p>
<p>Linux numbers the primary partitions 1, 2, 3 & 4. If you define an extended partitions, logical partitions inside it will be called 5, 6, 7.</p>
<p>Note: an Extended partition is just an empty box for creating Logical partitions inside it.</p>
```bash
/dev/sda3 is the 3rd primary partition on the first disk
/dev/sdb5 is the first logical partition on the second disk
/dev/sda7 is the 3rd logical partition of the first physical disk
```
- GPT (GUID Partition Table)
<p>If you format your disk with GTP you can have 128 primary partitions (no need to extended and logical).</p>

- SCSI device naming rule
```bash
# SCSI disk number rule
/dev/sda    disk number 1
/dev/sdb    disk number 2
/dev/sdc    disk number 3

# SCSI partition number rule
/dev/sda1   disk number 1, partition number 1
/dev/sdc3   disk number 3, partition number 3
```

- IDE device naming rule
```bash
# IDE disk number rule
/dev/hda    disk number 1
/dev/hdb    disk number 2
/dev/hdc    disk number 3
```

> image resource from https://ping-t.com














