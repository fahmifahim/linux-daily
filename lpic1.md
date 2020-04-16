```bash
# /etc/fstab
user: mount by everone, unmount by only one user
users: mount by everyone, unmount by everyone
nouser: no user can mount 
ro: read only
rw: read write
suid: suid and sgid available

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

#### * Regular Expression
![Regular Expression](https://ping-t.com/mondai3/img/jpg/k34024.jpg)

#### * nice - run a program with modified scheduling priority
```
$ nice [-n niceValue] command
```
![nice value](https://ping-t.com/mondai3/img/jpg/k34014.jpg)

#### * Archive (zip, bz2, tar, gzip)
- How to unzip file.bz2?
```bash
$ bunzip2 file.bz2
$ bzip2 -d file.bz2

```

#### * Devices
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

#### * Package
```bash
$ apt-get remove [package-name]
```
![apt-get](https://ping-t.com/mondai3/img/jpg/k33777.jpg)

> image resource from https://ping-t.com














