# 作业1：编译Linux内核
```
输入make x86_64_defconfig
```
![alt text](./第四期cicv训练营/image.png)
```
输入make LLVM=1 menuconfig
```
![alt text](./第四期cicv训练营/image-1.png)
```
输入make LLVM=1 -j$(nproc)
```
![alt text](./第四期cicv训练营/image-2.png)
编译完之后有vmlinux