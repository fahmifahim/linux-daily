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


#### Searching and Replacing with vi  
```bash
#The formal syntax for searching is:
:s/string

#For example, suppose you want to search some text for the string "cherry." Type the following and press ENTER:
:s/cherry

#The first match for "cherry" in your text will then be highlighted. To see if there are additional occurrences of the same string in the text, type n, and the highlight will switch to the next match, if one exists.


#The syntax for replacing one string with another string in the current line is
:s/pattern/replace/


#Here "pattern" represents the old string and "replace" represents the new string. For example, to replace each occurrence of the word "lemon" in a line with "orange," type:
:s/lemon/orange/



#The syntax for replacing every occurrence of a string in the entire text is similar. The only difference is the addition of a "%" in front of the "s":
:%s/pattern/replace/

#Thus repeating the previous example for the entire text instead of just for a single line would be:
:%s/lemon/orange/
```
