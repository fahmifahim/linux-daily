- [Read the Certificate text](https://github.com/fahmifahim/linux-daily/blob/master/linux.md#read-the-certificate-text)
- [Set hostname]

##### Read the Certificate text
```bash
$ openssl x509 -text -in /path/to/certificate.cert | less
```

##### Set hostname
```bash
# Set hostname
$ hostnamectl set-hostname [hostname-you-want-to-set]
# Check hostname
$ uname -n 
```
