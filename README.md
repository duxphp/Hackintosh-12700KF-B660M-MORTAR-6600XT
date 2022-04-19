# Hackintosh-12700KF-B660M-MORTAR-6600XT

适用于 12700KF + B660M迫击炮 DDR4 + 6600XT 黑苹果引导文件

基于 OpenCore 0.7.9 版本，机型 MacPro 7,1，系统 MacOS 12.3

本 EFI 参考其他基于 12代 引导与查阅资料，去除不必要的驱动并更新到最新版本

USB定制在15个端口内，保留内置 AX201 蓝牙与内置 JUSB-1 接口


# 本机配置

| 配置        | 型号                                 |
|-----------|------------------------------------|
| CPU       | intel i7 12700KF                   |
| 主板        | MSI MAG B660M MORTAR WiF DDR4      |
| 显卡        | 蓝宝石 AMD Radeon RX 6600XT 8G OC 超白金 |
| 内存        | 海盗船 3200MHz 16G * 2                |
| SSD       | 铠侠 RC20 1T NVME SSD                |
| 机箱        | 屌丝伯 D30 前面板 1USB 1 TYPE-C(USB转)    |
| 电源        | 鑫谷750w ATX                         |
| CPU 风扇    | 利民 PA120 SE                        |
| WiFi + 蓝牙 | BCM94360CD (PCI+USB转接卡)            |


# 使用情况
cpu正常，节能三项，睡眠正常，唤醒正常，usb2/3正常，声卡正常，wifi正常(禁用自带蓝牙和网卡)

# 避坑指南

### SSD

经真机测速 不支持 三星PM9A1、雷克沙NM800 状况为抹盘时卡在创建分区时或安装缓慢卡在重启安装阶段无限循环

金士顿 KC3000 有用户实测可以正常使用


# 其他说明

如果需要通过 OC 引导 Windows 请清除配置信息： Config—Misc—Security—scanpolicy 改为 0 


# BIOS 配置

本引导适用于 B660M 迫击炮主板，主板BIOS需一下设置


### 禁用：
Onboard CNVi Module Control-Disable Integrated

快速开机

Intel VT-D

CFG锁定

Speed Select Technology


### 开启：
Re-Size BAR Support

SR-IOV Support

电源 / err ready

# 更新记录

2022-04-19
更新 OC 到 0.8.0 更新驱动到最新版本


2022-03-26
- 取消WG驱动注入(MacPro机型不需要该驱动)显卡跑分变高
- 引导默认隐藏工具，且不引导windows分区
- 加入gpu温度传感器，取消显卡注入信息
- SMBIOS信息改为主板注入（引导windows后显示正确主板信息）

2022-03-25

基础版本，基于 OC 0.7.9


