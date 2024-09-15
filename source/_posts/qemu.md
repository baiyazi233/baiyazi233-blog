# 安装qemu
[qemu下载](https://www.qemu.org/download/)
```
解压qemu
sudo tar -xvJf qemu-7.2.12.tar.xz
cd qemu-7.2.12/
./configure
编译qemu
make -j 10
安装qemu
make install | tee make-install.log
```