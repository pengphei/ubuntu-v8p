# ubuntu-v8p

在 Dell Venue 8 Pro (3845) 上安装 ubuntu 系统。

该系统依赖 **uefi 32bit** 启动处理 **x86_64** 操作系统，因此我们需要对现有的 ubuntu 系统镜像进行处理。

## 系统配置

* 型号： Dell Venue 8 Pro 3845
* 内存： 1.0GB
* 处理器： Intel Atom CPU Z3735G @ 1.33GHz x 4
* 显卡：Intel@ HD Graphics (BYT)
* 存储： 32GB

## 镜像处理

### 环境依赖

1. 安装 ubuntu 20.04 系统
2. 下载本仓库中的 **isorespinner.sh** 脚本
3. 安装处理脚本依赖的软件包：

````
sudo apt install genisoimage dosfstools squashfs-tools xorriso p7zip-full bc curl klibc-utils iproute2 rsync unzip wget findutils
````

### ubuntu 18.04

1. 下载 ubuntu 18.04 镜像
2. 通过脚本处理 ubuntu 镜像：

````
isorespinner.sh -i ubuntu-18.04.6-desktop-amd64.iso -b GRUB-32
````

   最终生成新的镜像 **linuxium-ubuntu-18.04.6-desktop-amd64.iso**

### ubuntu 20.04

1. 下载 ubuntu 20.04 镜像
2. 通过脚本处理 ubuntu 镜像：

````
isorespinner.sh -i ubuntu-20.04.5-desktop-amd64.iso -b GRUB-32
````

   最终生成新的镜像 **linuxium-ubuntu-20.04.5-desktop-amd64.iso**