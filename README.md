---
output:
  pdf_document: default
  html_document: default
---
# dual-encrypt
Dual booting Windows 10 and ubuntu with full system ecryption


```bash
sudo pvcreate /dev/mapper/CryptDisk
sudo vgcreate vg0 /dev/mapper/CryptDisk
sudo lvcreate -n swap -L 2G vg0
sudo lvcreate -n root -L 10G vg0
sudo lvcreate -n home -l +100%FREE vg0
```
