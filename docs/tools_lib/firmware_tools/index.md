## 环境搭建介绍

### binwalk：

```
git clone https://github.com/devttys0/binwalk.git
cd binwalk
sudo ./deps.sh
sudo python ./setup.py install
sudo apt-get install python-lzma
sudo -H pip install git+https://github.com/ahupp/python-magic
sudo -H pip install git+https://github.com/sviehb/jefferson
```

### firmadyne：

```
git clone https://github.com/firmadyne/firmadyne
cd firmadyne/ && sudo download.sh
sudo -u postgres createuser -P firmadyne    password: firmadyne

sudo -u postgres createdb -O firmadyne firmware
sudo -u postgres psql -d firmware < ./firmadyne/database/schema
```

### qemu-2.4.0:

```
wget https://download.qemu.org/qemu-2.4.0.tar.xz
tar xvf qemu-2.4.0.tar.xz && cd qemu-2.4.0/
./configure --target-list=arm-softmmu,mips-softmmu,mipsel-softmmu --audio-drv-list=alsa,pa
make -j8
sudo make install
```

### gdb-multiarch:
```
sudo apt-get install gdb-multiarch
```
### gdbserver:

```
https://github.com/hugsy/gdb-static
```

### IDA 脚本

```
https://github.com/giantbranch/mipsAudit
https://github.com/tigerpuma/idatool-devttys0-
```

### Ghidra

```
https://www.nsa.gov/resources/everyone/ghidra/
```

### qemu_system_arm

```
https://people.debian.org/~aurel32/qemu/armhf/
```

### firmwalker

```
https://github.com/craigz28/firmwalker
```


## 工具库包含


### 交叉编译环境源码

### qemu 源码
- qemu-2.10
- qemu-2.5

#### qemu-trace

#### qemu-system

### IDA 插件
- mipsrop
- IDA_MIPS_EMU
- mipsAudit


### 静态编译程序（包含 mips、mipsel）

- netcat
- busybox
- gdbserver


### 一些厂商固件

- DLINK

### firmadyne 源码（包含 binary）
