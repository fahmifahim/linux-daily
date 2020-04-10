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
