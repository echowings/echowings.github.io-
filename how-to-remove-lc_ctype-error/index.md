# How to Remove LC_CTYPE Error




```
apt-get autoremove
export LC_ALL=en_US.UTF-8
echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen
locale-gen
```
