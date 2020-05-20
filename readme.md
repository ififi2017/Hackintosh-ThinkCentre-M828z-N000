# 本机配置
型号：Lenovo ThinkCentre M828z-N000

CPU：i5-9500

显卡：Intel UHD Graphics 630

RAM：DDR4 8GB

声卡：ALC235

有线网卡：Intel Ethernet Connection I219-V

硬盘：SAMSUNG NVME M.2 SSD PM981

# 说明

使用OpenCore 0.5.8 支持macOS 10.15.4。

## 安装方法
> 因为此款机型硬件特殊性，安装macOS时使用Kexts和SSDT与正常使用下均有不同。

### 带PM981固态硬盘的安装方法

1. 将Kexts文件夹下的HackrNVMeFamily.kext和APCI文件夹下的ssdt-nvme.aml移出备用。
2. 将macOS安装到其他硬盘（不能是PM981上），安装到第二阶段的自动重启后进入Windows。
3. 使用分区备份软件（如：Paragon Hard Disk Manager等同类软件。）使用备份或者复制的方式恢复到PM981上。
4. 将HackrNVMeFamily.kext和ssdt-nvme.aml放回原位，移出Kexts文件夹的NVMeFix.kext。
5. 继续安装，设置向导，安装完成。

### 非PM981固态硬盘的安装方法
1. 移除Kexts文件夹下的HackrNVMeFamily.kext、NVMeFix.kext和APCI文件夹下的ssdt-nvme.aml。
2. 按照正常安装步骤安装。

## BUG列表
- 睡眠
- 亮度
- ......

# 感谢列表 （排名不分先后）
[Intel Coffee Lake平台完美黑苹果系统安装教程（Opencore+Catalina15.4）](https://www.bilibili.com/video/BV1hA411t7dr "Intel Coffee Lake平台完美黑苹果系统安装教程（Opencore+Catalina15.4）")

[Coffee Lake - OpenCore Desktop Guide](https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/coffee-lake.html "OpenCore Desktop Guide - Coffee Lake")

[Display Configuration - OC-Laptop-Guide](https://1revenger1.gitbook.io/laptop-guide/prepare-install-macos/display-configuration#igpu-patching "Display Configuration - OC-Laptop-Guide")

[黑果小兵的部落格](https://blog.daliansky.net/ "黑果小兵的部落格")

[ACPI Hotpatch Samples for the OpenCore Bootloader](https://github.com/daliansky/OC-little "ACPI Hotpatch Samples for the OpenCore Bootloader")
