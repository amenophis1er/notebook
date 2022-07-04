List User added Root Certs:
---
```BASH
certutil -d sql:$HOME/.pki/nssdb -L
```
Add Root Cert
---
```BASH
certutil -d sql:$HOME/.pki/nssdb -A -t <TRUSTARGS> -n <certificate nickname> \
-i <certificate filename>
```
The `TRUSTARGS` are three strings of zero or more alphabetic characters, separated by commas. They define how the certificate should be trusted for SSL, email, and object signing, and are explained in the [certutil docs](https://firefox-source-docs.mozilla.org/security/nss/index.html#1034193)

For example, to trust a root CA certificate for issuing SSL server certificates, use

```BASH
certutil -d sql:$HOME/.pki/nssdb -A -t "C,," -n <certificate nickname> \
-i <certificate filename>
```
More info: [Chromium Linux Cert Management](https://chromium.googlesource.com/chromium/src/+/master/docs/linux/cert_management.md)

