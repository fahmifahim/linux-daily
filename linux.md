- [Read the Certificate text](https://github.com/fahmifahim/linux-daily/blob/master/linux.md#read-the-certificate-text)
- [Set hostname](https://github.com/fahmifahim/linux-daily/blob/master/linux.md#set-hostname)

##### Read the Certificate text
```bash
$ openssl x509 -text -in /path/to/certificate.cert | less
$ openssl x509 -noout -dates -in /path/to/certificate.cert 
```

##### Set hostname
```bash
# Set hostname
$ hostnamectl set-hostname [hostname-you-want-to-set]
# Check hostname
$ uname -n 
```

#### Mount shared NFS (temporary)  
```bash
$ mount -t nfs 192.168.0.100:/nfsshare /mnt/nfsshare

$ mount | grep nfs
        sunrpc on /var/lib/nfs/rpc_pipefs type rpc_pipefs (rw)
        nfsd on /proc/fs/nfsd type nfsd (rw)
        192.168.0.100:/nfsshare on /mnt type nfs (rw,addr=192.168.0.100)

# Unmount 
$ umount /mnt/nfsshare
```
