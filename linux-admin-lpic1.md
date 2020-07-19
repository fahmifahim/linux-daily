## Linux Basic for Administrator (LPIC 101 102)
- [Topic 101: System Architecture](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-topic-101-system-architecture)
  - [101.1 Determine and configure hardware settings](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1011-determine-and-configure-hardware-settings)
  - [101.2 Boot the system](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1012-boot-the-system)
  - [101.3 Change runlevels / boot targets and shutdown or reboot system](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1013-change-runlevels--boot-targets-and-shutdown-or-reboot-system)
- [Topic 102: Linux Installation and Package Management](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-topic-102-linux-installation-and-package-management)
  - [102.1 Design hard disk layout](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1021-design-hard-disk-layout)
  - [102.2 Install a boot manager](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1022-install-a-boot-manager)
  - [102.3 Manage shared libraries](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1023-manage-shared-libraries)
  - [102.4 Use Debian package management](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1024-use-debian-package-management)
  - [102.5 Use RPM and YUM package management](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1025-use-rpm-and-yum-package-management)
  - [102.6 Linux as a virtualization guest](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1026-linux-as-a-virtualization-guest)
- [Topic 103: GNU and Unix Commands](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-topic-103-gnu-and-unix-commands)
  - [103.1 Work on the command line](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1031-work-on-the-command-line)
  - [Process text streams using filters](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#1032-process-text-streams-using-filters)
  - [103.3 Perform basic file management](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1033-perform-basic-file-management)
  - [103.4 Use streams, pipes and redirects](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1034-use-streams-pipes-and-redirects)
  - [103.5 Create, monitor and kill processes](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1035-create-monitor-and-kill-processes)
  - [103.6 Modify process execution priorities](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1036-modify-process-execution-priorities)
  - [103.7 Search text files using regular expressions](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1037-search-text-files-using-regular-expressions)
- [ Topic 104: Devices, Linux Filesystems, Filesystem Hierarchy Standard](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-topic-104-devices-linux-filesystems-filesystem-hierarchy-standard)
  - [104.1 Create partitions and filesystems](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1041-create-partitions-and-filesystems)
  - [104.2 Maintain the integrity of filesystems](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#1042-maintain-the-integrity-of-filesystems)
  - [104.3 Control mounting and unmounting of filesystems](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#1043-control-mounting-and-unmounting-of-filesystems)
  - [104.5 Manage file permissions and ownership](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1045-manage-file-permissions-and-ownership)
  - [104.6 Create and change hard and symbolic links](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#1046-create-and-change-hard-and-symbolic-links)
  - [104.7 Find system files and place files in the correct location](https://github.com/fahmifahim/linux-daily/blob/master/linux-admin-lpic1.md#-1047-find-system-files-and-place-files-in-the-correct-location)

***
### # Topic 101: System Architecture
#### # 101.1 Determine and configure hardware settings

Weight: 2

*Description:* Candidates should be able to determine and configure fundamental system hardware

Key Knowledge Areas:
- Enable and disable integrated peripherals.
- Differentiate between the various types of mass storage devices.
- Determine hardware resources for devices.
- Tools and utilities to list various hardware information (e.g. lsusb, lspci, etc.).
- Tools and utilities to manipulate USB devices.
- Conceptual understanding of sysfs, udev and dbus.

The following is a partial list of the used files, terms and utilities:
- /sys/
- /proc/
- /dev/
- modprobe
- lsmod
- lspci
- lsusb

**/proc** 
| FileName | Details | 
| :--- | :--- |
| /proc/interrupts | IRQ information | 
| /proc/ioports | I/O address | 
| /proc/bus/pci/devices | PCI device | 
| /proc/bus/usb/devices | USB device | 
| /proc/meminfo | Memory information | 
| /proc/cpuinfo | CPU information | 
| /proc/dma | DMA channel information | 
| /proc/modules | Loaded modules information | 


**lsusb** - list USB devices
```bash
$ lsusb
Bus 002 Device 002: ID 8087:0020 Intel Corp. Integrated Rate Matching Hub
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 002: ID 8087:0020 Intel Corp. Integrated Rate Matching Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

$ cat /proc/bus/usb/devices
...
```


***
#### # 101.2 Boot the system
Weight: 3

*Description:* Candidates should be able to guide the system through the booting process.

*Key Knowledge Areas:*
- Provide common commands to the boot loader and options to the kernel at boot time.
- Demonstrate knowledge of the boot sequence from BIOS/UEFI to boot completion.
- Understanding of SysVinit and systemd.
- Awareness of Upstart.
- Check boot events in the log files.

The following is a partial list of the used files, terms and utilities:
- dmesg
- journalctl
- BIOS
- UEFI
- bootloader
- kernel
- initramfs
- init
- SysVinit
- systemd

### # Boot Linux System
#### 1. BIOS
- BIOS is Basic Input Output System and does the first steps of the PC bootup. For example is does a POST (Power On Self Test) and decides which hardware should boot the system.
- PowerON --> BIOS --> Recognize HDD and decide the device priority by order. 
- On each device: read the MBR (Master Boot Record) located on head sector. Bootloader is then executed.
- Device priority can be set manually on BIOS display. 
- Currently, other than BIOS, UEFI (Unified Extensible Firmware Interface) is recently developed and widely being used in the modern system. 

#### 2. bootloader
<p>Bootloader can be GRUB (1&2) or LILO which are great for disks less than 2TB.</p>

```bash
/etc/lilo.conf
/boot/grub/grub.cfg
/boot/grub/menu.lst
```

#### 3. Kernel
- Kernel parameters (sometimes called boot parameters) supply the kernel with information about hardware parameters that it might not determine on its own - say single user mod boot (S)
- Recognize and control hardware; then, performs various initialization processes such as mounting root file system.
- Kernel image, kernel version is located on /boot directory. 
- Start the /sbin/init
- Parameters passed to the kernel at the time it is started is defined in `/proc/cmdline`
  ```bash
  $ cat /proc/cmdline
  BOOT_IMAGE=/vmlinuz-3.10.0-957.el7.x86_64 root=UUID=f1f52244-7b2d-4383-b6ac-367d09e57a09 ro crashkernel=auto rhgb quiet LANG=en_US.UTF-8

  # GRUB Legacy
  grub> kernel [kernel-image] [option]
  grub> kernel /boot/vmlinuz init=/bin/bash

  # GRUB2
  grub> linux /boot/vmlinuz init=/bin/bash quiet
  ```

#### 4. init
- When the kernel finishes loading, it usually starts /sbin/init. This program remains running until the system is shutdown. 
- It is always assigned PID 1 for init process.
- In SysVinit system, /sbin/init is started during the initial process. Autostart application is executed by order as recorded in the `/etc/inittab`. 
- In recent/modern system (like `systemd`), /etc/inittab is no more used.  

#### dmesg
- Funny fact: During the bootup, only The Kernel is running so it should record and keep its own logs!
- dmesg command will show the full data from kernel ring buffer up to now. 
```bash
# Print or control the kernel ring buffer
$ dmesg
$ journalctl -k
$ journalctl --dmesg
[996822.568071] userif-3: sent link down event.
[996822.568078] userif-3: sent link up event.
[996823.415945] wlp16s0: authenticate with 50:c4:dd:3b:8d:08

# Clear the dmesg log
$ dmesg --clear

```

#### /var/log/messages
- After the init process comes up, syslog daemon will log messages. It has timestamps and will persist during restarts.
- Kernel is still logging its own messages in dmesg.

#### initramfs
- The only purpose of an initramfs is to mount the root filesystem. The initramfs is a complete set of directories that you would find on a normal root filesystem. It is bundled into a single cpio archive and compressed with one of several compression algorithms.
- At boot time, the boot loader loads the kernel and the initramfs image into memory and starts the kernel. The kernel checks for the presence of the initramfs and, if found, mounts it as / and runs /init. The init program is typically a shell script. Note that the boot process takes longer, possibly significantly longer, if an initramfs is used.
- It is located on /boot directory

#### # journalctl
- journalctl config file: /etc/systemd/journald.conf
```bash
# Check log based on unit
$ journalctl -u systemd-resolved.service
$ journalctl -u 'systemd*'
$ journalctl -u '*docker*'

# Specify time using --since(-S) and --until(-U)
$ journalctl --since today
$ journalctl -S "2020-01-01 11:00:00" -U "2020-01-02 12:00:00"

# Specify the Priority
"emerg" 0
"alert" 1  
"crit" 2  
"err" 3  
"warning" 4  
"notice" 5
"info" 6  
"debug" 7 
$ journalctl -p [priority-number]
$ journalctl -p 3
... : Failed to start Network Manager Wait Online...

# Tail the new entry
$ journalctl -f -u '*docker*'
```

***
#### # 101.3 Change runlevels / boot targets and shutdown or reboot system
Weight: 3

*Description:* Candidates should be able to manage the SysVinit runlevel or systemd boot target of the system. This objective includes changing to single user mode, shutdown or rebooting the system. Candidates should be able to alert users before switching runlevels / boot targets and properly terminate processes. This objective also includes setting the default SysVinit runlevel or systemd boot target. It also includes awareness of Upstart as an alternative to SysVinit or systemd.

*Key Knowledge Areas:*
- Set the default runlevel or boot target.
- Change between runlevels / boot targets including single user mode.
- Shutdown and reboot from the command line.
- Alert users before switching runlevels / boot targets or other major system events.
- Properly terminate processes.
- Awareness of acpid.

The following is a partial list of the used files, terms and utilities:
- /etc/inittab
- shutdown
- init
- /etc/init.d/
- telinit
- systemd
- systemctl
- /etc/systemd/
- /usr/lib/systemd/
- wall

#### # SysVinit
- /sbin/init is started during the initial process. Autostart application is executed by order as recorded in the `/etc/inittab`.
- If you edit the /etc/inittab and want to make the change directly to the system without rebooting, you may execute the below command: 
  ```bash
  init q
  init Q
  telinit q
  telinit Q
  ```
- Single-User system, start the script from `/etc/rc1.d`
- Multi-User system, start the script from `/etc/rc3.d`
- Rules: 
  - The start script for Each RunLevel is determined: 
    ```bash
    /etc/rc[0-6].d
    RunLevel: 
    0 = poweroff
    1 = rescue / single user
    2,3,4 = multi-user
    5 = graphical
    6 = reboot
    ```
  - Script file name is determined: 
    ```bash
    First word: K (kill) or S (start)
    Number: priority number
    ServiceName
    Example: K01Bluetooth
    ```
  - As mentioned above, in Single-User system, the appropriate Kill script name for Blueetooth process: `/etc/rc1.d/K01Bluetooth`

#### # Telinit
```bash
# Power-off the machine. 
telinit 0 
systemctl poweroff.target
shutdown -h now

# Reboot the machine. 
telinit 6
systemctl reboot.target
shutdown -r now
reboot
```


#### # RunLevel
```bash
$ runlevel
N 5
```
![RunLevel](https://ping-t.com/mondai3/img/jpg/kkk34236.jpg)


#### # Shutdown 
```bash
# Currently at 22:00 and will shutdown the system on 23:00
$ shutdown -h +60
$ shutdown -h 23:00
$ shutdown -r 23:00 "Rebooting in 60 minutes"
$ shutdown -r +60 "Rebooting in 60 minutes"
```

#### # Systemctl command
- structure: `systemctl [subcommand] [Unit-name]`
- subcommand: 
```bash
# systemctl subcommand with unit-name
disable
enable
is-active
start
stop
restart
status
reload

# systemctl subcommand without unit-name
list-unit-files
get-default
halt
reboot
poweroff
```

- More about systemctl
```bash
$ ls -l /etc/systemd/system
default.target -> /lib/systemd/system/multi-user.target
default.target.wants
multi-user.target.wants
socket.target.wants
system-update.target.wants

# For example observe the httpd
$ systemctl status httpd
httpd.service 
Loaded: loaded (/usr/lib/systemd/system/httpd.service): enable

$ ls /etc/systemd/system/multi-user.target.wants
/etc/systemd/system/multi-user.target.wants -> /usr/lib/systemd/system/httpd.service
```

![systemd](https://upload.wikimedia.org/wikipedia/commons/3/35/Systemd_components.svg)

![architecture](https://upload.wikimedia.org/wikipedia/commons/e/e7/Linux_kernel_unified_hierarchy_cgroups_and_systemd.svg)

***
### # Topic 102: Linux Installation and Package Management
#### # 102.1 Design hard disk layout

Weight: 2

*Description:* Candidates should be able to design a disk partitioning scheme for a Linux system.

Key Knowledge Areas:
- Allocate filesystems and swap space to separate partitions or disks.
- Tailor the design to the intended use of the system.
- Ensure the /boot partition conforms to the hardware architecture requirements for booting.
- Knowledge of basic features of LVM.

The following is a partial list of the used files, terms and utilities:
- / (root) filesystem
- /var filesystem
- /home filesystem
- /boot filesystem
- EFI System Partition (ESP)
- swap space
- mount points
- partitions

#### # Hard Disk Design
- Physical Volume (pv): a whole drive or a partition. It is better to define partitions and not use whole disks - unpartitioned.
- Volume Groups (vg): this is the collection of one or more pvs. OS will see the vg as one big disk. PVs in one vg, can have different sizes or even be on different physical disks.
- Logical Volumes (lv): OS will see lvs as partitions. You can format an lv wit your OS and use it.
![pv-vg-lv](https://ping-t.com/mondai3/img/jpg/k34230.jpg)
  - `pvcreate`
  - `vgcreate`
  - `lvcreate`

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
Note: an Extended partition is just an empty box for creating Logical partitions inside it.

```bash
/dev/sda3 is the 3rd primary partition on the first disk
/dev/sdb5 is the first logical partition on the second disk
/dev/sda7 is the 3rd logical partition of the first physical disk
```
![MBR](https://ping-t.com/mondai3/img/jpg/k34058.jpg)

- GPT (GUID Partition Table)
  - 128 primary partitions are available (no need to extended and logical).
  - Maximum storage 9.4ZB. 
  - UEFI (Unified Extensible Firmware Interface) is needed. 

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

***

#### # 102.2 Install a boot manager

Weight: 2

Description: Candidates should be able to select, install and configure a boot manager.

Key Knowledge Areas:
- Providing alternative boot locations and backup boot options.
- Install and configure a boot loader such as GRUB Legacy.
- Perform basic configuration changes for GRUB 2.
- Interact with the boot loader.

The following is a partial list of the used files, terms and utilities:
- menu.lst, grub.cfg and grub.conf
- grub-install
- grub-mkconfig
- MBR


#### # Maintenance Mode on Grub
```bash
# Single Mode
$ grub > kernel /boot/vmlinuz-2.6.35 s
$ grub > kernel /boot/vmlinuz-2.6.35 1
$ grub > kernel /boot/vmlinuz-2.6.35 single
```

![grub](https://ping-t.com/mondai3/img/jpg/kk33690.jpg)


***
#### # 102.3 Manage shared libraries

Weight: 1

Description: Candidates should be able to determine the shared libraries that executable programs depend on and install them when necessary.

*Key Knowledge Areas:*
- Identify shared libraries.
- Identify the typical locations of system libraries.
- Load shared libraries.

The following is a partial list of the used files, terms and utilities:
- ldd
  - the ldd command helps you find:
    - If a program is dynamically or statically linked
    - What libraries a program needs
    ```bash
    $ ldd /sbin/ldconfig
    not a dynamic executable
    
    $ ldd /bin/ls
    ls     lsblk  lsmod  
    linux-vdso.so.1 =>  (0x00007fffef1fc000)
    libselinux.so.1 => /lib/x86_64-linux-gnu/libselinux.so.1 (0x00007f61696b3000)
    libacl.so.1 => /lib/x86_64-linux-gnu/libacl.so.1 (0x00007f61694aa000)    
    ```
- Shared library setting: 
  1. Config the library to /etc/ld.so.conf 
  ```bash
  $ vi /etc/ld.so.conf
  /home/test/mylib    --> Add this path as your own lib
  ```
    - Update the setting by executing the `ldconfig` command
    ```bash
    $ ldconfig
    ```
    - ldconfig will update the `/etc/ld.so.cache`
    
  2. Set the library path to LD_LIBRARY_PATH
  - Use this variable if you need to override the original installed libraries and use your own or a specific library. 
    ```bash
    $ export  LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/test/mylib
    ```

- Common library directory
```bash
/lib
/lib64
/usr/lib
/usr/lib64
```

*Linking*
1. *Static linking* is when you add this library to your executable program. In this method your program size is big because it has all the needed libraries. One good advantage is your program can be run without being dependent to other programs / libraries.
2. *Dynamic linking* is when you just say in your program "We need this and that library to run this program". This way your program is smaller but you need to install those libraries separately. This makes programs more secure (because libraries can be updated centrally), more advanced (any improvement in a library will improve the whole program) and smaller.

***

#### # 102.4 Use Debian package management

Weight: 3

*Description:* Candidates should be able to perform package management using the Debian package tools.

Key Knowledge Areas:
- Install, upgrade and uninstall Debian binary packages.
- Find packages containing specific files or libraries which may or may not be installed.
- Obtain package information like version, content, dependencies, package integrity and installation status (whether or not the package is installed).
- Awareness of apt.

The following is a partial list of the used files, terms and utilities:
- /etc/apt/sources.list
- dpkg
- dpkg-reconfigure
- apt-get
- apt-cache

#### # dpkg - Debian package manager
```bash
$ dpkg [option] action

# dpkg skip same version -E, --skip-same-version
$ dpkg -Ei procmail_3.22-16_i386.deb
$ dpkg -E --install procmail_3.22-16_i386.deb

# Search for a filename from installed packages.
$ dpkg --search /usr/share/doc/ssh
$ dpkg -S /usr/share/doc/ssh

# Install all packages recursively from directory
$ dpkg -Ri /directory
$ dpkg --recursive --install

# Refuse downgrade --refuse-downgrade
$ dpkg -Gi packages
```

![dpkg-command](https://ping-t.com/mondai3/img/jpg/k33766.jpg)

##### apt-get
```bash
# Remove specific package
$ apt-get remove [package-name]

# Upgrade all packages
$ apt-get upgrade
```
![apt-get](https://ping-t.com/mondai3/img/jpg/k33777.jpg)

##### apt-cache
- apt-cache is purposed to provide information about the Debian package database
```bash
# Search for a program
$ apt-cache search [keyword]

# Display detail information 
$ apt-cache show [package-name]

# Display package information
$ apt-cache showpkg [package-name]

# Display dependencies
$ apt-cache depends [package-name]
```

##### aptitude
- update
- show [package-name]
- search [pattern]
- install [package-name]
- remove [package-name]
- download [package-name]
- upgrade [package-name]

***

#### # 102.5 Use RPM and YUM package management

Weight: 3

*Description:* Candidates should be able to perform package management using RPM, YUM and Zypper.

Key Knowledge Areas:
- Install, re-install, upgrade and remove packages using RPM, YUM and Zypper.
- Obtain information on RPM packages such as version, status, dependencies, integrity and signatures.
- Determine what files a package provides, as well as find which package a specific file comes from.
- Awareness of dnf.

The following is a partial list of the used files, terms and utilities:
- rpm
- rpm2cpio
- /etc/yum.conf
- /etc/yum.repos.d/
- yum
- zypper

##### rpm - RPM Package Manager
```bash
# Find 
$ rpm --query --list postfix
$ rpm -ql posftfix

# Find dependency on package
$ rpm --query --requires --package emacs
$ rpm -qRp emacs

# Find change history on specific RPM package
$ rpm -q --changelog nfs-utils-1.3.0-0.61.el7.x86_64
```
- <b>query</b></br>
![rpm](https://ping-t.com/mondai3/img/jpg/k35692.jpg)

- <b>install</b></br>
![rpm-install](https://ping-t.com/mondai3/img/jpg/k33792.jpg)

##### zypper - SUSE based package manager
```bash
$ zypper [option] subcommand
-- subcommand: 
  install | in  -- install package
  update | up   -- update package
  remove | rm   -- uninstall package
  info          -- display detail information of package
  search | se   -- search package by entering keyword
  list-updates | lu -- list updateable package
  repos | lr    -- show list of repository
  refresh       -- update repository
```

**yum**
- `/etc/yum.repos.d`
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

***

#### # 102.6 Linux as a virtualization guest

Weight: 1

Description: Candidates should understand the implications of virtualization and cloud computing on a Linux guest system.

Key Knowledge Areas:
- Understand the general concept of virtual machines and containers.
- Understand common elements virtual machines in an IaaS cloud, such as computing instances, block storage and networking.
- Understand unique properties of a Linux system which have to changed when a system is cloned or used as a template.
- Understand how system images are used to deploy virtual machines, cloud instances and containers.
- Understand Linux extensions which integrate Linux with a virtualization product.
- Awareness of cloud-init.

The following is a partial list of the used files, terms and utilities:
- Virtual machine
- Linux container
- Application container
- Guest drivers
- SSH host keys
- D-Bus machine id

***

### # Topic 103: GNU and Unix Commands
#### # 103.1 Work on the command line

Weight: 4

Description: Candidates should be able to interact with shells and commands using the command line. The objective assumes the Bash shell.

Key Knowledge Areas:
- Use single shell commands and one line command sequences to perform basic tasks on the command line.
- Use and modify the shell environment including defining, referencing and exporting environment variables.
- Use and edit command history.
- Invoke commands inside and outside the defined path.

The following is a partial list of the used files, terms and utilities:
- bash
- echo
- env
- export
- pwd
- set
- unset
- type
- which
- man
- uname
- history
- .bash_history
- Quoting

#### # Environment
```bash
# Show variable to the Environment 
$ env - print environment variables. 
$ printenv - print environment variables. It can't see local ones
$ set - built-in shell command, it shows shell-local variables (including shell functions)

$ export var1=val1  # Define var1 as environment variable
$ var2=val2         # Define var2 as local variable
$ env | egrep var[1,2]
    var1=val1       # env can't see the local variable
$ printenv | egrep var[1,2]
    var1=val1       # printenv can't see the local variable
$ set | egrep var[1,2]
    var1=val1
    var2=val2

```
![printenv](https://ping-t.com/mondai3/img/jpg/k34146.jpg)

#### # history
```bash
$ echo $HISTFILE
/root/.bash_history

$ echo $HISTSIZE
1000

$ history
```


***

#### 103.2 Process text streams using filters
Weight: 2

*Description:* Candidates should be able to apply filters to text streams.

*Key Knowledge Areas:*
- Send text files and output streams through text utility filters to modify the output using standard UNIX commands found in the GNU textutils package.

The following is a partial list of the used files, terms and utilities:
- cat
- bzcat
- xzcat
- zcat
- nl
- cut
- sed
- tr
- uniq
- sort
- head
- less
- md5sum
- od
- paste
- sha256sum
- sha512sum
- split
- tail
- wc

#### # vi / vim 
![tune2fs](https://ping-t.com/mondai3/img/jpg/k33911.jpg)


- sed - stream editor for filtering and transforming text
```bash
$ sed -e s/pingt/hoge/g test.txt
$ sed s/pingt/hoge/g test.txt 
```
![sed](https://ping-t.com/mondai3/img/jpg/k34032.jpg)


#### # Windows CRLF and Linux LF
- Windows: CRLF \r\n
- Linux: LF \n
```bash
# Change Windows format to Linux compatible
$ tr -d '^M' < file1.txt > file2.txt
$ tr -d '\r' < file1.txt > file2.txt
$ cat file1.txt | tr -d '\r' > file2.txt
$ sed s/^M//g file1.txt > file2.txt
```


- tr - Translate, squeeze, and/or delete characters from standard input, writing to standard output.
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

*Line number*
- cat and nl
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

$ nl -b file.txt
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

- tail 
```bash
$ tail -n 3 httpd.conf
# line1
# line2
# line3

$ tail -f /Logs/OS/messages

```

- od
```bash
$ cat file1.txt
hello
goodbye

$ cat file1.txt | od -c
$ od -t c file1.txt
0000000   h   e   l   l   o  \n   g   o   o   d   b   y   e  \n
0000017

$ od -t cx2 file1.txt
0000000   h   e   l   l   o  \n   g   o   o   d   b   y   e  \n
           6568    6c6c    0a6f    6f67    646f    7962    0a65
0000016


Traditional format specifications may be intermixed; they accumulate:
       -a     same as -t a,  select named characters, ignoring high-order bit

       -b     same as -t o1, select octal bytes

       -c     same as -t c,  select printable characters or backslash escapes

       -d     same as -t u2, select unsigned decimal 2-byte units

       -f     same as -t fF, select floats

       -i     same as -t dI, select decimal ints

       -l     same as -t dL, select decimal longs

       -o     same as -t o2, select octal 2-byte units

       -s     same as -t d2, select decimal 2-byte units

       -x     same as -t x2, select hexadecimal 2-byte units
```


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

***

#### # 103.3 Perform basic file management

Weight: 4

Description: Candidates should be able to use the basic Linux commands to manage files and directories.

Key Knowledge Areas:
- Copy, move and remove files and directories individually.
- Copy multiple files and directories recursively.
- Remove files and directories recursively.
- Use simple and advanced wildcard specifications in commands.
- Using find to locate and act on files based on type, size, or time.
- Usage of tar, cpio and dd.

The following is a partial list of the used files, terms and utilities:
- cp
- find
- mkdir
- mv
- ls
- rm
- rmdir - remove empty directories
- touch
- tar
- cpio
- dd
- file
- gzip
- gunzip
- bzip2
- bunzip2
- xz
- unxz
- file globbing

#### # File access timestamp
- *stat*
```bash
$ stat test.txt
File: 'test.txt'
Size: 4
Access: (0644/-rw-r--r--)
Context: unconfined_u:object_r:admin_home_t:s0
Access: 2020-01-01 10:00:00
Modify: 2020-01-01 10:00:00
Change: 2020-01-01 10:00:00

# Access time stamp CHANGED after the file command
$ file test.txt
text.txt ASCII text

$ stat test.txt
...
Access: 2020-01-01 11:00:00
...

# Access/Modify/Change Time stamp change after the `touch` `echo`
$ touch test.txt
$ echo "hello" > test.txt
$ stat test.txt
...
Access: 2020-01-02 10:00:00
Modify: 2020-01-02 10:00:00
Change: 2020-01-02 10:00:00
...
```

#### * Archive (tar, bz2, xz, gzip) -> [reference](https://jadi.gitbooks.io/lpic1/content/1033_perform_basic_file_management.html)
1. tar 
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

2. bz2 - How to unzip file.bz2?</br>
<b>Notes:</b> bzip2 only works with file
```bash
$ bunzip2 file.bz2
$ bzip2 -d file.bz2

# How to make file.bz2
$ bzip2 file.txt
-> file.txt.bz2 is created
```

3. xz 
```bash
$ xz [option] file-name-to-compress
[option]: 
-d --decompress
-k --keep
-l --list
```

4. gzip 
```bash
# Compress with gzip
$ ls -l aaa.txt
    -rwx------ 2 fahmi fahmi 25 Jul 18 16:26 aaa.txt

$ cat aaa.txt
    aaaa
    bbbb
    bbbb
    bbbb
    bbbb

$ gzip -c aaa.txt > aaa.gz

$ ls -l | grep aaa
    -rw-r--r-- 1 root  root   37 Jul 19 17:15 aaa.gz
    -rwx------ 2 fahmi fahmi  25 Jul 18 16:26 aaa.txt

# Decompress with gzip
$ gzip -d aaa.gz

$ ls -l | grep aaa
    -rw-r--r-- 1 root  root   25 Jul 19 17:15 aaa
    -rwx------ 2 fahmi fahmi  25 Jul 18 16:26 aaa.txt

$ diff aaa aaa.txt
# no difference
```


***
 
#### # 103.4 Use streams, pipes and redirects

Weight: 4

Description: Candidates should be able to redirect streams and connect them in order to efficiently process textual data. Tasks include redirecting standard input, standard output and standard error, piping the output of one command to the input of another command, using the output of one command as arguments to another command and sending output to both stdout and a file.

Key Knowledge Areas:
- Redirecting standard input, standard output and standard error.
- Pipe the output of one command to the input of another command.
- Use the output of one command as arguments to another command.
- Send output to both stdout and a file.

The following is a partial list of the used files, terms and utilities:
- tee
- xargs

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

***

#### # 103.5 Create, monitor and kill processes

Weight: 4

*Description:* Candidates should be able to perform basic process management.

Key Knowledge Areas:
- Run jobs in the foreground and background.
- Signal a program to continue running after logout.
- Monitor active processes.
- Select and sort processes for display.
- Send signals to processes.

The following is a partial list of the used files, terms and utilities:
- &
- bg
- fg
- jobs
- kill
- nohup
- ps
- top
- free
- uptime
- pgrep
- pkill
- killall
- watch
- screen
- tmux

**foreground and background jobs**
![fgbg](https://raw.githubusercontent.com/fahmifahim/linux-daily/master/images/background_foreground.jpg)

- Normally if you run a program on the terminal, it blocks your terminal but sending a command to the background will prevent this:
```bash
xeyes &
```
- But what if we started it normally? We can break / cancel it with Ctrl+c or suspend it using Ctrl+z.
```bash
$ xeyes 
^Z
[1]+  Stopped                 xeyes

$ jobs
[1]+  Stopped                 xeyes

$ bg
[1]+ xeyes &

$ jobs
[1]+  Running                 xeyes &

$ sleep 1000 & 
[2] 7395

$ jobs
[1]-  Running                 xeyes &
[2]+  Running                 sleep 1000 &

$ fg %2
sleep 1000
^Z
[2]+  Stopped                 sleep 1000

$ jobs
[1]-  Running                 xeyes &
[2]+  Stopped                 sleep 1000

$ bg sle
[2]+ sleep 1000 &

$ jobs
[1]-  Running                 xeyes &
[2]+  Running                 sleep 1000 &
```
> -l switch of jobs will also show the process ID

**nohup**
- The nohup command lets you run your commands even after you logged out and writes its output to nohup.out:
```bash
$ nohup ping 4.2.2.4
nohup: ignoring input and appending output to enohup.outf
^C

$ cat nohup.out 
PING 4.2.2.4 (4.2.2.4) 56(84) bytes of data.
64 bytes from 4.2.2.4: icmp_seq=1 ttl=51 time=225 ms
64 bytes from 4.2.2.4: icmp_seq=3 ttl=51 time=223 ms

--- 4.2.2.4 ping statistics ---
4 packets transmitted, 2 received, 50% packet loss, time 3010ms
rtt min/avg/max/mdev = 223.584/224.767/225.950/1.183 ms
```
> It is common to use 2> to redirect the nohup errors to a file: nohup script.sh > mynohup.out 2>&1 &

### # Process
#### # Kill Process
1. kill - terminate a process
</br>You can control processes by using signals. Actually pressing Ctrl+c and Ctrl+z is also sending signals. Another way for this is using the kill command:
- kill using job number
```bash
$ jobs
[4]   Running                 sleep 1000 &
[5]-  Running                 sleep 2000 &
[6]+  Running                 sleep 3000 &

$ kill %4

$ jobs
[4]   Terminated              sleep 1000
[5]-  Running                 sleep 2000 &
[6]+  Running                 sleep 3000 &

$ jobs
[5]-  Running                 sleep 2000 &
[6]+  Running                 sleep 3000 &
```
- kill using pid
```bash
$ ps -ef | grep -Ei "ppid|sleep"
UID         PID   PPID  C STIME TTY          TIME CMD
root      10837   9464  0 22:05 pts/0    00:00:00 sleep 2000
root      10877   9464  0 22:09 pts/0    00:00:00 sleep 4000

$ kill 10837

$ ps -ef | grep -Ei "ppid|sleep"
UID         PID   PPID  C STIME TTY          TIME CMD
root      10877   9464  0 22:09 pts/0    00:00:00 sleep 4000
root      10881   9464  0 22:10 pts/0    00:00:00 grep --color=auto -Ei ppid|sleep
[2]-  Terminated              sleep 2000
```

- kill using signal name (pkill = kill using process name)

![kill-signal](https://ping-t.com/mondai3/img/jpg/k34001.jpg)

```bash
$ ps -ef | grep -Ei "ppid|sleep"
UID         PID   PPID  C STIME TTY          TIME CMD
root      10912   9464  0 22:17 pts/0    00:00:00 sleep 6000      -> KILL
root      10919   9464  0 22:18 pts/0    00:00:00 sleep 7000      -> TERMINATE
root      10920   9464  0 22:18 pts/0    00:00:00 sleep 8000

$ kill -9 10912
$ kill -s 9 10912
$ kill -KILL 10912
$ kill -s KILL 10912
$ kill -SIGKILL 10912
$ kill -s SIGKILL 10912

$ kill -15 10919
$ kill -s 15 10919
$ kill -TERM 10919
$ kill -s TERM 10919
$ kill -SIGTERM 10919
$ kill -s SIGTERM 10919

$ pkill -9 sleep        --> kill all sleep process

$ ps -ef | grep -Ei "ppid|sleep"
UID         PID   PPID  C STIME TTY          TIME CMD
root      10920   9464  0 22:18 pts/0    00:00:00 sleep 8000
[5]+  Killed                  sleep 6000
[6]-  Terminated              sleep 7000
```


#### # Monitoring Process
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

# To see the process in tree
$ ps axf
  PID TTY      STAT   TIME COMMAND
  655 ?        Ss     0:00 /usr/sbin/crond -n
  659 tty1     Ss+    0:00 /sbin/agetty --noclear tty1 linux
  897 ?        Ss     0:00 /usr/sbin/sshd -D
 4990 ?        Ss     0:00  \_ sshd: root@pts/0
 5011 pts/0    Ss     0:00      \_ -bash
 6734 pts/0    R+     0:00          \_ ps axf
 6735 pts/0    S+     0:00          \_ lessq 
```
![ps-process](https://ping-t.com/mondai3/img/jpg/k34339.jpg)

2. top </br>
Processes are changing and sometimes you need to check them live. top command will help you. </br>

3. free - Display amount of free and used memory in the system
```bash
$ free -h 
              total        used        free      shared  buff/cache   available
Mem:           972M        139M        549M         13M        283M        656M
Swap:          1.5G          0B        1.5G
```

4. uptime - Tell how long the system has been running.
```bash
$ uptime
 21:51:30 up 20:25,  2 users,  load average: 0.00, 0.01, 0.05
```

***

#### # 103.6 Modify process execution priorities

Weight: 2

*Description:* Candidates should should be able to manage process execution priorities.

Key Knowledge Areas:
- Know the default priority of a job that is created.
- Run a program with higher or lower priority than the default.
- Change the priority of a running process.

The following is a partial list of the used files, terms and utilities:
- nice
- ps
- renice
- top

**nice**  - run a program with modified scheduling priority
**renice** - alter priority of running processes
```bash
$ nice [-n niceValue] command

# Set test1 to top priority
$ nice -n -20 test1
$ nice --20 test1

# Set an already run process (pid 100) to top priority
$ renice -20 -p 100
$ renice -20 100
```
![nice value](https://ping-t.com/mondai3/img/jpg/k34014.jpg)


***

#### # 103.7 Search text files using regular expressions

Weight: 3

*Description:* Candidates should be able to manipulate files and text data using regular expressions. This objective includes creating simple regular expressions containing several notational elements as well as understanding the differences between basic and extended regular expressions. It also includes using regular expression tools to perform searches through a filesystem or file content.

Key Knowledge Areas:
- Create simple regular expressions containing several notational elements.
- Understand the differences between basic and extended regular expressions.
- Understand the concepts of special characters, character classes, quantifiers and anchors.
- Use regular expression tools to perform searches through a filesystem or file content.
- Use regular expressions to delete, change and substitute text.

The following is a partial list of the used files, terms and utilities:
- grep
- egrep
- fgrep
- sed
- regex(7)

#### # Regular Expression
![Regular Expression](https://ping-t.com/mondai3/img/jpg/k34024.jpg)

#### # Metacharacter
![Metacharacter](https://ping-t.com/mondai3/img/jpg/k33833.jpg)

*grep*
```bash
grep [option]

-F, --fixed-strings, --fixed-regexp
              Interpret  PATTERN  as  a  list of fixed strings, separated by newlines, any of which is to be matched.
-E, --extended-regexp
              Interpret PATTERN as an extended regular expression (ERE, see below).
-n, --line-number
              Prefix each line of output with the 1-based line number within its input file.
-i, --ignore-case
              Ignore case distinctions in both the PATTERN and the input files.
-v, --invert-match
              to select non-matching lines.
-c, --count
              Suppress normal output; instead print a count of matching lines for each input file.
```
- Sample for grep 
```bash
$ cat test.txt
PINGT
PingT
pingt
.*

$ grep '\.\*' test.txt
$ fgrep '.*' test.txt
$ grep -F '.*' test.txt
.*  --> Result the same

```


***
### # Topic 104: Devices, Linux Filesystems, Filesystem Hierarchy Standard
#### # 104.1 Create partitions and filesystems
Weight: 2

*Description:* Candidates should be able to configure disk partitions and then create filesystems on media such as hard disks. This includes the handling of swap partitions.

*Key Knowledge Areas:*
- Manage MBR and GPT partition tables
- Use various mkfs commands to create various filesystems such as:
  - ext2/ext3/ext4
  - XFS
  - VFAT
  - exFAT
- Basic feature knowledge of Btrfs, including multi-device filesystems, compression and subvolumes.

The following is a partial list of the used files, terms and utilities:
- fdisk
- gdisk
- parted
- mkfs
- mkswap

##### *mkfs*
```bash
$ mkfs [option] [device-name]
$ mkfs -t ext3 -c /dev/sda2
$ mkfs -t ext4 /dev/sdc1
```
![mkfs](https://ping-t.com/mondai3/img/jpg/k34068.jpg)

##### *mkswap*
```bash
$ mkswap /dev/sda6
```

##### *xfs* 

![xfs-command](https://ping-t.com/mondai3/img/jpg/k34083.jpg)

##### *Btrfs*
- Available for multidevice
```bash
mkfs.btrfs /dev/sda1 /dev/sda2
```
- Snapshot for subvolume
```bash
btrfs subvolume snapshot /home /tmp/home_bak
```
- Auto-archive function

**File System**
| File System | Details | 
| :--- | :--- | 
| ext2 | Standard file system for traditional Linux | 
| ext3 | Nextgen ext2, Journaling filesystem  |
| ext4 | Nextgen ext3, Journaling filesystem |
| XFS | Developed by Silicongraphics, Journaling filesystem, Dynamic inode |
| JFS | Developed by IBM, Journaling filesystem, Dynamic inod |

***
#### 104.2 Maintain the integrity of filesystems
Weight: 2

*Description:* Candidates should be able to maintain a standard filesystem, as well as the extra data associated with a journaling filesystem.

*Key Knowledge Areas:*
- Verify the integrity of filesystems.
- Monitor free space and inodes.
- Repair simple filesystem problems.

The following is a partial list of the used files, terms and utilities:
- du
- df
- fsck
- e2fsck
  ```bash
  # automatically select "yes" for the question
  $ e2fsck -y /dev/sda4
  # Automatically repair ("preen") the file system
  $ e2fsck -p /dev/sda4
  ```
- mke2fs
- tune2fs
- xfs_repair - repair an XFS filesystem
- xfs_fsr - filesystem reorganizer for XFS
- xfs_db - debug an XFS filesystem
- xfs_check - check an XFS filesystem


#### # Filesystem
1. tune2fs - adjust tunable filesystem parameters on ext2/ext3/ext4 filesystems
```bash
$ tune2fs [option] DeviceName
$ tune2fs -L /WORK /dev/hda5
```
![tune2fs](https://ping-t.com/mondai3/img/jpg/k34080.jpg)


##### *du disk usage*
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

##### *mke2fs*
```bash
$ mke2fs [option] [device-name]
$ mke2fs -j /dev/sda2     --> create ext3 FileSystem
$ mke2fs -t ext2 /dev/sda2
$ mke2fs -t ext3 /dev/sda2
```

![mke2fs](https://ping-t.com/mondai3/img/jpg/kk34068.jpg)

***

#### 104.3 Control mounting and unmounting of filesystems
Weight: 3

*Description:* Candidates should be able to configure the mounting of a filesystem.

*Key Knowledge Areas:*
- Manually mount and unmount filesystems.
- Configure filesystem mounting on bootup.
- Configure user mountable removable filesystems.
- Use of labels and UUIDs for identifying and mounting file systems.
- Awareness of systemd mount units.

The following is a partial list of the used files, terms and utilities:
- /etc/fstab
- /media/
- mount
- umount
- blkid
- lsblk

**fstab**
- /etc/fstab
  1. File system: 
    - Label -> LABEL=/boot
    - UUID -> UUID=01240174917-1401924ohfaqgh
    - device -> /dev/sda1
  2. Mount point: swap or none for swap
  3. Type: can be auto
  4. Mount options: defaults, rw / ro, noauto, user, exec / noexec, noatime
  5. Dump flag: 0 no dump, 1 dump activate. Mostly 0
  6. pass: Non-zero values of pass specify the order of checking filesystems at boot time (seen in Integrity of file systems)
```bash
# /etc/fstab
user: mount by everyone, unmount by only one user
users: mount by everyone, unmount by everyone
nouser: no user can mount 
ro: read only
rw: read write
suid: suid and sgid available
```

![fstab](https://ping-t.com/mondai3/img/jpg/k34089.jpg)

**mount**
```bash
# Mount all content on /etc/fstab
$ mount -a 

# Set the mount type (-t) and additional option (-o)
$ mount -t ext3 -o ro /dev/sda3 /mnt/mydata

# Bind directory
$ ls systemlogs
  --> Before mount nothing happen
$ mount --bind /var/log /root/systemlogs

$ ls systemlogs
  --> Display all files on /var/log 
```

- All these command replies the same values: 
  - `mount`
  - `cat /etc/mtab`
  - `cat /proc/mounts`
  - `cat /proc/self/mounts`

![mount](https://ping-t.com/mondai3/img/jpg/k34088.jpg)

**umount**
```bash
$ umount -a
$ umount /mnt/mydata
```

![umounts](https://ping-t.com/mondai3/img/jpg/kk34088.jpg)

***

#### # 104.4 Removed

***
 
#### # 104.5 Manage file permissions and ownership

Weight: 3

Description: Candidates should be able to control file access through the proper use of permissions and ownerships.

Key Knowledge Areas:
- Manage access permissions on regular and special files as well as directories.
- Use access modes such as suid, sgid and the sticky bit to maintain security.
- Know how to change the file creation mask.
- Use the group field to grant file access to group members.

The following is a partial list of the used files, terms and utilities:
- chmod
- umask
- chown
- chgrp

#### # File and Directory Permission (SUID, SGID, Stickybit)

- SUID SGID Stickybit

| Access Mode | Octal | Symbolic |
|:---:|:---:|:---:|
|suid |4000 |u+s |
|guid |2000 |g+s |
|stickybit |1000 |t |


- File and Directory permission 

| Permission | File | Directory |
|:---:|:---:|:---:|
| Read | Read file content (cat,more,less) | List and refer content of directory (ls,find) |
| Write | Write to file | Create, delete and rename file (touch,mv,rm) |
| eXecute | execute file | Access to file inside directory, change to directory (cd) |

```bash
d------r-- root:root /read.d
  |-- [---------x root:root]  /read.d/execute.txt
  |-- [-------r-- root:root]  /read.d/read.txt
  '-- [--------w- root:root]  /read.d/write.txt

d-------w- root:root /write.d
  |-- [---------x root:root]  /read.d/execute.txt
  |-- [-------r-- root:root]  /read.d/read.txt
  '-- [--------w- root:root]  /read.d/write.txt

d--------x root:root /execute.d
  |-- [---------x root:root]  /read.d/execute.txt
  |-- [-------r-- root:root]  /read.d/read.txt
  '-- [--------w- root:root]  /read.d/write.txt

# List and find content inside the folder
$ su fahmi
$ ls /read.d/
 ls: cannot access /read.d/read.txt: Permission denied
 ls: cannot access /read.d/write.txt: Permission denied
 ls: cannot access /read.d/execute.txt: Permission denied
 execute.txt  read.txt  write.txt
$ ls /read.d/ | wc -l
 3
$ find /read.d/ -type f
 /read.d/read.txt
 /read.d/write.txt
 /read.d/execute.txt

---
$ ls /write.d/
 ls: cannot open directory /write.d/: Permission denied
$ find /write.d/ -type f
 find: '/write.d/': Permission denied

---
$ ls /execute.d/
 ls: cannot open directory /execute.d/: Permission denied
$ find /execute.d/ -type f
 find: '/execute.d/': Permission denied
 
 # Change Directory 
 $ cd /read.d/
bash: cd: /read.d/: Permission denied

]$ cd /write.d/
bash: cd: /write.d/: Permission denied

$ cd /execute.d/
[execute.d]$

```


***

#### 104.6 Create and change hard and symbolic links
Weight: 2

*Description:* Candidates should be able to create and manage hard and symbolic links to a file.

*Key Knowledge Areas:*
- Create links.
- Identify hard and/or soft links.
- Copying versus linking files.
- Use links to support system administration tasks.

The following is a partial list of the used files, terms and utilities:
- ln
- ls

*Symbolic link*: 
1. Link can be created even in different file system.
2. `lrwxr-xr-x symlink1 -> test1.txt`
3. Symbolic link file has different inode with the physical file.
4. If we delete the physical file, symbolic link will not be deleted. But there will be error if we show the content of the symbolic link.
5. Symbolic link works with file and folder. 

![symboliclink](https://ping-t.com/mondai3/img/jpg/kkkk34107.jpg)

*Hard link*:
1. Hardlink has the same inode with the physical file.
2. Deleting the physical file, will not effect hardlink. 
3. Hardlink works with file, NOT folder.

![hardlink](https://ping-t.com/mondai3/img/jpg/k34107.jpg)

```bash
Usage: ln [OPTION]... [-T] TARGET LINK_NAME   (1st form)
  or:  ln [OPTION]... TARGET                  (2nd form)
  or:  ln [OPTION]... TARGET... DIRECTORY     (3rd form)
  or:  ln [OPTION]... -t DIRECTORY TARGET...  (4th form)

$ ls -il
8613901762 -rw-r--r--   1 fahmi  staff    6 Apr 22 11:09 test1.txt

# Create Symbolic link for file
$ ln -s test1.txt symlink1
# Create Symbolic link for directory
$ ln -s dir1/ dir-symlink1

# Create Hard link (ONLY for FILE)
$ ln -n test1.txt hardlink1
# ERROR for folder
$ ln -n folder1 hardlinkFolder1
ln: 'hardlinkFolder1': hard link not allowed for directory

$ ls -il
8613901762 -rw-r--r--   2 fahmi  staff    6 Apr 22 11:09 test1.txt
8613901762 -rw-r--r--   2 fahmi  staff    6 Apr 22 11:09 hardlink1
8613901770 lrwxr-xr-x   1 fahmi  staff    9 Apr 22 11:09 symlink1 -> test1.txt
269011342 lrwxrwxrwx 1 root root  5 May  2 15:22 dir-symlink1 -> dir1/
269011185 drwxr-xr-x 2 root root  6 May  2 15:19 dir1

# Remove link
$ unlink symlink1
$ unlink dir-symlink1
```

***
#### # 104.7 Find system files and place files in the correct location

Weight: 2

*Description:* Candidates should be thoroughly familiar with the Filesystem Hierarchy Standard (FHS), including typical file locations and directory classifications.

Key Knowledge Areas:
- Understand the correct locations of files under the FHS.
- Find files and commands on a Linux system.
- Know the location and purpose of important file and directories as defined in the FHS.

The following is a partial list of the used files, terms and utilities:
- find
- locate
- updatedb
- /etc/updatedb.conf
- whereis
- which
- type

#### # Filesystem Hierarchy Standard ([FHS wikipedia](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard))
![FHS](https://ping-t.com/mondai3/img/jpg/k34123.jpg)

- directory structure

![directory](https://ping-t.com/mondai3/img/jpg/k33739.jpg)

#### # locate and updatedb
- `find` can search files and directory, but it is slow. 
- `locate` could do faster than `find` 

```bash
And it is fast:
$ time locate kernel | wc -l 
11235

real    0m0.341s
user    0m0.322s
sys    0m0.015s
```
- This is fast because its data comes from a database created with `updatedb` command which is usually run on a daily basis with a cron job. Its configuration file is `/etc/updatedb.conf` or `/etc/sysconfig/locate`:

```bash
$ cat /etc/updatedb.conf 
PRUNE_BIND_MOUNTS="yes"
# PRUNENAMES=".git .bzr .hg .svn"
PRUNEPATHS="/tmp /var/spool /media /home/.ecryptfs"
PRUNEFS="NFS nfs nfs4 rpc_pipefs afs binfmt_misc proc smbfs autofs iso9660 ncpfs coda devpts ftpfs devfs mfs shfs sysfs cifs lustre tmpfs usbfs udf fuse.glusterfs fuse.sshfs curlftpfs ecryptfs fusesmb devtmpfs"
```

- You can update the db by running `updatedb` as root and get some info about it by -S switch of locate command:
```bash
$ locate -S
Database /var/lib/mlocate/mlocate.db:
    73,602 directories
    711,894 files
    46,160,154 bytes in file names
    18,912,999 bytes used to store database
```
***


### # Topic 105: Shells and Shell Scripting
#### # 105.1 Customize and use the shell environment

Weight: 4

Description: Candidates should be able to customize shell environments to meet users' needs. Candidates should be able to modify global and user profiles.

Key Knowledge Areas:
- Set environment variables (e.g. PATH) at login or when spawning a new shell.
- Write Bash functions for frequently used sequences of commands.
- Maintain skeleton directories for new user accounts.
- Set command search path with the proper directory.

The following is a partial list of the used files, terms and utilities:
- .
- source
- /etc/bash.bashrc
- /etc/profile
- env
- export
- set
- unset
- ~/.bash_profile
- ~/.bash_login
- ~/.profile
- ~/.bashrc
- ~/.bash_logout
- function
- alias

*** 

#### # 105.2 Customize or write simple scripts

Weight: 4

Description: Candidates should be able to customize existing scripts, or write simple new Bash scripts.

Key Knowledge Areas:
- Use standard sh syntax (loops, tests).
- Use command substitution.
- Test return values for success or failure or other information provided by a command.
- Execute chained commands.
- Perform conditional mailing to the superuser.
- Correctly select the script interpreter through the shebang (#!) line.
- Manage the location, ownership, execution and suid-rights of scripts.

The following is a partial list of the used files, terms and utilities:
- for
- while
- test
- if
- read
- seq
- exec
- ||
- &&

*** 

### # Topic 106: User Interfaces and Desktops
#### # 106.1 Install and configure X11

Weight: 2

Description: Candidates should be able to install and configure X11.

Key Knowledge Areas:
- Understanding of the X11 architecture.
- Basic understanding and knowledge of the X Window configuration file.
- Overwrite specific aspects of Xorg configuration, such as keyboard layout.
- Understand the components of desktop environments, such as display managers and window managers.
- Manage access to the X server and display applications on remote X servers.
- Awareness of Wayland.

The following is a partial list of the used files, terms and utilities:
- /etc/X11/xorg.conf
- /etc/X11/xorg.conf.d/
- ~/.xsession-errors
- xhost
- xauth
- DISPLAY
- X

***
#### # 106.2 Graphical Desktops

Weight: 1

Description: Candidates should be aware of major Linux desktops. Furthermore, candidates should be aware of protocols used to access remote desktop sessions.

Key Knowledge Areas:
- Awareness of major desktop environments
- Awareness of protocols to access remote desktop sessions

The following is a partial list of the used files, terms and utilities:
- KDE
- Gnome
- Xfce
- X11
- XDMCP
- VNC
- Spice
- RDP

***

#### # 106.3 Accessibility

Weight: 1

Description: Demonstrate knowledge and awareness of accessibility technologies.

Key Knowledge Areas:
- Basic knowledge of visual settings and themes.
- Basic knowledge of assistive technology.

The following is a partial list of the used files, terms and utilities:
- High Contrast/Large Print Desktop Themes.
- Screen Reader.
- Braille Display.
- Screen Magnifier.
- On-Screen Keyboard.
- Sticky/Repeat keys.
- Slow/Bounce/Toggle keys.
- Mouse keys.
- Gestures.
- Voice recognition.

***

### # Topic 107: Administrative Tasks
#### # 107.1 Manage user and group accounts and related system files

Weight: 5

Description: Candidates should be able to add, remove, suspend and change user accounts.

Key Knowledge Areas:
- Add, modify and remove users and groups.
- Manage user/group info in password/group databases.
- Create and manage special purpose and limited accounts.

The following is a partial list of the used files, terms and utilities:
- /etc/passwd
- /etc/shadow
- /etc/group
- /etc/skel/
- chage
- getent
- groupadd
- groupdel
- groupmod
- passwd
- useradd
- userdel
- usermod

***

#### # 107.2 Automate system administration tasks by scheduling jobs

Weight: 4

Description: Candidates should be able to use cron and systemd timers to run jobs at regular intervals and to use at to run jobs at a specific time.

Key Knowledge Areas:
- Manage cron and at jobs.
- Configure user access to cron and at services.
- Understand systemd timer units.

The following is a partial list of the used files, terms and utilities:
- /etc/cron.{d,daily,hourly,monthly,weekly}/
- /etc/at.deny
- /etc/at.allow
- /etc/crontab
- /etc/cron.allow
- /etc/cron.deny
- /var/spool/cron/
- crontab
- at
- atq
- atrm
- systemctl
- systemd-run

***

#### # 107.3 Localisation and internationalisation

Weight: 3

Description: Candidates should be able to localize a system in a different language than English. As well, an understanding of why LANG=C is useful when scripting.

Key Knowledge Areas:
- Configure locale settings and environment variables.
- Configure timezone settings and environment variables.

The following is a partial list of the used files, terms and utilities:
- /etc/timezone
- /etc/localtime
- /usr/share/zoneinfo/
- LC_*
- LC_ALL
- LANG
- TZ
- /usr/bin/locale
- tzselect
- timedatectl
- date
- iconv
- UTF-8
- ISO-8859
- ASCII
- Unicode

***

### # Topic 108: Essential System Services
#### # 108.1 Maintain system time

Weight: 3

Description: Candidates should be able to properly maintain the system time and synchronize the clock via NTP.

Key Knowledge Areas:
- Set the system date and time.
- Set the hardware clock to the correct time in UTC.
- Configure the correct timezone.
- Basic NTP configuration using ntpd and chrony.
- Knowledge of using the pool.ntp.org service.
- Awareness of the ntpq command.

The following is a partial list of the used files, terms and utilities:
- /usr/share/zoneinfo/
- /etc/timezone
- /etc/localtime
- /etc/ntp.conf
- /etc/chrony.conf
- date
- hwclock
- timedatectl
- ntpd
- ntpdate
- chronyc
- pool.ntp.org

***

#### # 108.2 System logging

Weight: 4

Description: Candidates should be able to configure rsyslog. This objective also includes configuring the logging daemon to send log output to a central log server or accept log output as a central log server. Use of the systemd journal subsystem is covered. Also, awareness of syslog and syslog-ng as alternative logging systems is included.

Key Knowledge Areas:
- Basic configuration of rsyslog.
- Understanding of standard facilities, priorities and actions.
- Query the systemd journal.
- Filter systemd journal data by criteria such as date, service or priority.
- Configure persistent systemd journal storage and journal size.
- Delete old systemd journal data.
- Retrieve systemd journal data from a rescue system or file system copy.
- Understand interaction of rsyslog with systemd-journald.
- Configuration of logrotate.
- Awareness of syslog and syslog-ng.

Terms and Utilities:
- /etc/rsyslog.conf
- /var/log/
- logger
- logrotate
- /etc/logrotate.conf
- /etc/logrotate.d/
- journalctl
- systemd-cat
- /etc/systemd/journald.conf
- /var/log/journal/

***

#### # 108.3 Mail Transfer Agent (MTA) basics

Weight: 3

Description: Candidates should be aware of the commonly available MTA programs and be able to perform basic forward and alias configuration on a client host. Other configuration files are not covered.

Key Knowledge Areas:
- Create e-mail aliases.
- Configure e-mail forwarding.
- Knowledge of commonly available MTA programs (postfix, sendmail, exim) (no configuration).

Terms and Utilities:
- ~/.forward
- sendmail emulation layer commands
- newaliases
- mail
- mailq
- postfix
- sendmail
- exim

***

#### # 108.4 Manage printers and printing

Weight: 2

Description: Candidates should be able to manage print queues and user print jobs using CUPS and the LPD compatibility interface.

Key Knowledge Areas:
- Basic CUPS configuration (for local and remote printers).
- Manage user print queues.
- Troubleshoot general printing problems.
- Add and remove jobs from configured printer queues.

The following is a partial list of the used files, terms and utilities:
- CUPS configuration files, tools and utilities
- /etc/cups/
- lpd legacy interface (lpr, lprm, lpq)

***

### # Topic 109: Networking Fundamentals
#### # 109.1 Fundamentals of internet protocols

Weight: 4

Description: Candidates should demonstrate a proper understanding of TCP/IP network fundamentals.

- Key Knowledge Areas:
- Demonstrate an understanding of network masks and CIDR notation.
- Knowledge of the differences between private and public "dotted quad" IP addresses.
- Knowledge about common TCP and UDP ports and services (20, 21, 22, 23, 25, 53, 80, 110, 123, 139, 143, 161, 162, 389, 443, 465, 514, 636, 993, 995).
- Knowledge about the differences and major features of UDP, TCP and ICMP.
- Knowledge of the major differences between IPv4 and IPv6.
- Knowledge of the basic features of IPv6.

The following is a partial list of the used files, terms and utilities:
- /etc/services
- IPv4, IPv6
- Subnetting
- TCP, UDP, ICMP

***

#### # 109.2 Persistent network configuration

Weight: 4

Description: Candidates should be able to manage the persistent network configuration of a Linux host.

Key Knowledge Areas:
- Understand basic TCP/IP host configuration.
- Configure ethernet and wi-fi network using NetworkManager.
- Awareness of systemd-networkd.

The following is a partial list of the used files, terms and utilities:
- /etc/hostname
- /etc/hosts
- /etc/nsswitch.conf
- /etc/resolv.conf
- nmcli
- hostnamectl
- ifup
- ifdown

***

#### # 109.3 Basic network troubleshooting

Weight: 4

Description: Candidates should be able to troubleshoot networking issues on client hosts.

Key Knowledge Areas:
- Manually configure network interfaces, including viewing and changing the configuration of network interfaces using iproute2.
- Manually configure routing, including viewing and changing routing tables and setting the default route using iproute2.
- Debug problems associated with the network configuration.
- Awareness of legacy net-tools commands.

The following is a partial list of the used files, terms and utilities:
- ip
- hostname
- ss
- ping
- ping6
- traceroute
- traceroute6
- tracepath
- tracepath6
- netcat
- ifconfig
- netstat
- route

***

#### # 109.4 Configure client side DNS

Weight: 2

Description: Candidates should be able to configure DNS on a client host.

Key Knowledge Areas:
- Query remote DNS servers.
- Configure local name resolution and use remote DNS servers.
- Modify the order in which name resolution is done.
- Debug errors related to name resolution.
- Awareness of systemd-resolved.

The following is a partial list of the used files, terms and utilities:
- /etc/hosts
- /etc/resolv.conf
- /etc/nsswitch.conf
- host
- dig
- getent

***

### # Topic 110: Security
#### # 110.1 Perform security administration tasks

Weight: 3

Description: Candidates should know how to review system configuration to ensure host security in accordance with local security policies.

Key Knowledge Areas:
- Audit a system to find files with the suid/sgid bit set.
- Set or change user passwords and password aging information.
- Being able to use nmap and netstat to discover open ports on a system.
- Set up limits on user logins, processes and memory usage.
- Determine which users have logged in to the system or are currently logged in.
- Basic sudo configuration and usage.

The following is a partial list of the used files, terms and utilities:
- find
- passwd
- fuser
- lsof
- nmap
- chage
- netstat
- sudo
- /etc/sudoers
- su
- usermod
- ulimit
- who, w, last

***

#### # 110.2 Setup host security

Weight: 3

Description: Candidates should know how to set up a basic level of host security.

Key Knowledge Areas:
- Awareness of shadow passwords and how they work.
- Turn off network services not in use.
- Understand the role of TCP wrappers.

The following is a partial list of the used files, terms and utilities:
- /etc/nologin
- /etc/passwd
- /etc/shadow
- /etc/xinetd.d/
- /etc/xinetd.conf
- systemd.socket
- /etc/inittab
- /etc/init.d/
- /etc/hosts.allow
- /etc/hosts.deny

***

#### # 110.3 Securing data with encryption

Weight: 4

Description: The candidate should be able to use public key techniques to secure data and communication.

Key Knowledge Areas:
- Perform basic OpenSSH 2 client configuration and usage.
- Understand the role of OpenSSH 2 server host keys.
- Perform basic GnuPG configuration, usage and revocation.
- Use GPG to encrypt, decrypt, sign and verify files.
- Understand SSH port tunnels (including X11 tunnels).

The following is a partial list of the used files, terms and utilities:
- ssh
- ssh-keygen
- ssh-agent
- ssh-add
- ~/.ssh/id_rsa and id_rsa.pub
- ~/.ssh/id_dsa and id_dsa.pub
- ~/.ssh/id_ecdsa and id_ecdsa.pub
- ~/.ssh/id_ed25519 and id_ed25519.pub
- /etc/ssh/ssh_host_rsa_key and ssh_host_rsa_key.pub
- /etc/ssh/ssh_host_dsa_key and ssh_host_dsa_key.pub
- /etc/ssh/ssh_host_ecdsa_key and ssh_host_ecdsa_key.pub
- /etc/ssh/ssh_host_ed25519_key and ssh_host_ed25519_key.pub
- ~/.ssh/authorized_keys
- ssh_known_hosts
- gpg
- gpg-agent
- ~/.gnupg/

***

Future Change Considerations

Future changes to the objective will/may include:
- Remove ifup/ifdown and legacy net-tools command
- Remove TCP wrappers


</br> *Image resource from [ping-t.com](https://ping-t.com)
</br> *Reference book [jadi-lpic1-book](https://jadi.gitbooks.io/lpic1/content/)



## Others
#### SELinux context
- Reference: [RedHat Guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/selinux_users_and_administrators_guide/sect-security-enhanced_linux-working_with_selinux-selinux_contexts_labeling_files) 
- SELinux context = user:role:type:level

```bash
# Check SELinux enforcing mode
$ getenforce
   Enforcing

# Check the SELinux context
$ ls -ldZ /folder1
   drwxr-xr-x root root unconfined_u:object_r:etc_t:s0 /folder1

$ ls -lZ /folder1/file1.txt
   -rw-r--r--  root root unconfined_u:object_r:etc_t:s0 /folder1/file1.txt
   
```

- Temporary Change (this change doesn't survive system relabel, or `restorecon` command)
```bash
$ chcon -t <type> <file-pah | folder-path>
$ chcon -t httpd_sys_content_t /folder1
$ chcon -t httpd_sys_content_t /folder1/file1

$ chcon -R -t httpd_sys_content_t /folder2   # Change recursively
```

- Persistent Context Change
  - semanage fcontext 
  - restorecon
```bash
# Adding new recorde
# Enter the following command, remembering to use the full path to the file or directory:
semanage fcontext -a options file-name|directory-name

# Use the restorecon utility to apply the context changes:
restorecon -v file-name|directory-name


# Modify recorde
# Enter the following command, remembering to use the full path to the file or directory:
semanage fcontext -m options file-name|directory-name

# Use the restorecon utility to apply the context changes:
restorecon -v file-name|directory-name
```

- Sample
```bash
semanage fcontext -a -t <type> <file-pah | folder-path>
semanage fcontext -a httpd_sys_content_t /folder1

-or to modify-

semanage fcontext -m -t <type> <file-pah | folder-path>
semanage fcontext -m -t httpd_sys_content_t /folder1

# Don't forget to make it permanent by `restorecon`
restorecon -v <file-pah | folder-path>
restorecon -v /folder1
   unconfined_u:object_r:etc_t:s0->system_u:object_r:httpd_sys_content_t:s0

```

#### Network Check
```bash
# Destination IP address to check = 1.2.3.4
# Source IP = 4.3.2.1
# Test the ping connection
ping 1.2.3.4

# Scan the available port
nmap 1.2.3.4
nmap -sT -p 443 1.2.3.4  # -sT : if the port is TCP protocol, -sU for UDP
nmap -sT -p 80 1.2.3.4 -e eth1 4.3.2.1 
```

#### awk
```bash
echo Hello1 > file1111.txt
echo Hello2 > file2222.txt
echo Hello3 > file3333.txt
echo Hello4 > test4444.txt

ls
    file1111.txt  file2222.txt  file3333.txt  test4444.txt

ls | grep file | awk '{print "cat "$1}'
    cat file1111.txt
    cat file2222.txt
    cat file3333.txt

ls | grep file | awk '{print "cat "$1}' | sh
    Hello1
    Hello2
    Hello3
```


##### Certificate openssl
```bash
# Certificate expire dates
openssl x509 -noout -dates -in [certificate-full-path]

# Certificate full information
openssl x509 -text -in [certificate-full-path]
```

##### Find duplicate entries on text file
```bash
# Assume you have log file as follows: 
cat log1.txt
    AAAAAA BBBBB CCCCC 1
    AAAAAA BBBBB CCCCC 2
    AAAAAA BBBBB CCCCC 3    # duplicate entry
    AAAAAA BBBBB CCCCC 3    # duplicate entry
    AAAAAA BBBBB CCCCC 4
    AAAAAA BBBBB CCCCC 5    # duplicate entry
    AAAAAA BBBBB CCCCC 6
    AAAAAA BBBBB CCCCC 7
    AAAAAA BBBBB CCCCC 8
    AAAAAA BBBBB CCCCC 5    # duplicate entry
    AAAAAA BBBBB CCCCC 9
    AAAAAA BBBBB CCCCC 10

# Sort message at index 4. Sort this item as number
cat log1.txt | sort -n -k 4
    AAAAAA BBBBB CCCCC 1
    AAAAAA BBBBB CCCCC 2
    AAAAAA BBBBB CCCCC 3  # duplicate entry
    AAAAAA BBBBB CCCCC 3  # duplicate entry
    AAAAAA BBBBB CCCCC 4
    AAAAAA BBBBB CCCCC 5  # duplicate entry
    AAAAAA BBBBB CCCCC 5  # duplicate entry
    AAAAAA BBBBB CCCCC 6
    AAAAAA BBBBB CCCCC 7
    AAAAAA BBBBB CCCCC 8
    AAAAAA BBBBB CCCCC 9
    AAAAAA BBBBB CCCCC 10

# Sort message and only show the uniq entry
cat log1.txt | sort -n -k 4 | uniq
    AAAAAA BBBBB CCCCC 1
    AAAAAA BBBBB CCCCC 2
    AAAAAA BBBBB CCCCC 3
    AAAAAA BBBBB CCCCC 4
    AAAAAA BBBBB CCCCC 5
    AAAAAA BBBBB CCCCC 6
    AAAAAA BBBBB CCCCC 7
    AAAAAA BBBBB CCCCC 8
    AAAAAA BBBBB CCCCC 9
    AAAAAA BBBBB CCCCC 10

# Sort, show uniq entry and count the uniqness of each entry
cat log1.txt | sort -n -k 4 | uniq -c
    1 AAAAAA BBBBB CCCCC 1
    1 AAAAAA BBBBB CCCCC 2
    2 AAAAAA BBBBB CCCCC 3
    1 AAAAAA BBBBB CCCCC 4
    2 AAAAAA BBBBB CCCCC 5
    1 AAAAAA BBBBB CCCCC 6
    1 AAAAAA BBBBB CCCCC 7
    1 AAAAAA BBBBB CCCCC 8
    1 AAAAAA BBBBB CCCCC 9
    1 AAAAAA BBBBB CCCCC 10

# Find entry which has 2 duplicate entries
cat log1.txt | sort -n -k 4 | uniq -c | awk '{print $1" "$2" "$3" "$4" "$5}' | grep ^2
    2 AAAAAA BBBBB CCCCC 3
    2 AAAAAA BBBBB CCCCC 5
```
