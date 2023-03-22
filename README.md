# OSLab_XV6
Well.....This is my first lab for learning OS. 



# Lab0:

搭建好了环境，参考了b站`BV11K4y127Qk`的视频

安装Ubuntu 20.04

换源

           sudo apt update
    
           sudo apt upgrade

```
sudo apt install git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-linux-gnu binutils-riscv64-linux-gnu libglib2.0-dev libpixman-1-dev gcc-riscv64-unknown-elf 

wget https://download.qemu.org/qemu-5.1.0.tar.xz

tar xvf qemu-5.1.0.tar.xz

cd qemu-5.1.0

./configure --disable-kvm --disable-werror --prefix=/usr/local --target-list="riscv64-softmmu"
```

如若第7步报错，则去知乎查看“踩坑之旅”

```
make

sudo make install
```

检测安装

```
riscv64-unknown-elf-gcc --version
```

预期：riscv64-unknown-elf-gcc (GCC) 10.1.0

```
qemu-system-riscv64 --version
```

预期：QEMU emulator version 5.1.0

```
git clone git://g.csail.mit.edu/xv6-labs-2020

cd xv6-labs-2020

git checkout util
```

预期：

Branch 'util' set up to track remote branch 'util' from 'origin'.

  Switched to a new branch 'util'

```
make qemu
```

使用ctrl-a x退出



注意gitignore qemu 太大了
