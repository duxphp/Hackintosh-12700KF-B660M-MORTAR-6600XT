# Hackintosh-12700KF-B660M-MORTAR-6600XT

适用于 12700KF + B660M迫击炮 DDR4 + 6600XT 黑苹果引导文件

基于 OpenCore 0.7.9 版本，机型 MacPro 7,1，系统 MacOS 12.3

本 EFI 参考其他基于 12代 引导与查阅资料，去除不必要的驱动并更新到最新版本

USB定制在15个端口内，保留内置 AX201 蓝牙与内置 JUSB-1 接口


# 本机配置

| 配置        | 型号                                                   |
|-----------|------------------------------------------------------|
| CPU       | intel i7 12700KF / intel i5 12600KF                  |
| 主板        | MSI MAG B660M MORTAR WiF DDR4  / MSI Z690 刀锋钛 DDR4   |
| 显卡        | 蓝宝石 AMD Radeon RX 6600XT 8G OC 超白金 / 蓝宝石 RX6900XT 毒药 |
| 内存        | 海盗船 3200MHz 16G * 2 / 酷兽 DDR4 8G * 4                 |
| SSD       |  铠侠 RD20 512G NVME SSD / 大华C970 PRO         |
| 机箱        | 屌丝伯 D30 前面板 1USB 1 TYPE-C(USB转)                      |
| 电源        | 鑫谷750w ATX                                           |
| CPU 风扇    | 利民 PA120 SE                                          |
| WiFi + 蓝牙 | 主板自带 intel AX201                                     |


# 使用情况
cpu正常，节能三项，睡眠正常，唤醒正常，usb2/3正常，声卡正常，wifi正常

新增主机 12600KF + 6900XT 改配置无需修改可安装使用，需要根据机箱定制USB

# 避坑指南

### SSD

#### 不支持的硬盘 

三星PM9A1

雷克沙NM800

状况为抹盘时卡在创建分区时或安装缓慢卡在重启安装阶段无限循环


#### 支持的硬盘

西数系列

铠侠系列

金士顿 KC3000


# 其他说明

如果需要通过 OC 引导 Windows 请清除配置信息： Config—Misc—Security—scanpolicy 改为 0 

经过长期使用测试，mac pro 机型不需要加载 WhateverGreen.kext 驱动同时也不需要配套防的补丁 agdpmod=pikera 默认已取消该驱动加载

该引导同样适用于 12代 大小核设计CPU，12600及以上，请在 BIOS 禁用核显

请自行填写系统生成三码


# BIOS 配置

本引导适用于 B660M 迫击炮主板，主板BIOS需以下设置，请将bios更新到最新版本 7D42v17 及以上


### 禁用：

SETTING - 安全引导

OC - CPU特征 VT-D


### 开启：

BETA - D.T.M

BETA - SR-IOV Support

SETTING - ACPI - Re-Size BAR Support


# 更新记录

2022-12-13
- 更新intel wifi驱动到最新测试版 - 请勿启用WG驱动
- 注入6600xt CFG_LINK_FIXED_MAP 解决登录黑屏登录界面分辨率不一致

2022-12-08

- 同步 OC 至 0.8.7
- 更新intel wifi驱动到最新测试版，解决开机链接慢的问题
- 更新intel 蓝牙驱动到最新测试版，解决睡眠唤醒重启问题

2022-11-18

- 同步 OC 至 0.8.6

2022-11-04

- 重新定制 CPUFriendDataProvider 变频驱动，让cpu跑分变频正常

2022-10-25

#### 该版本为 macos 13 版本，macos12版本更新会导致intel网卡无法使用，仅供 macos13 使用，该版本的intel wifi驱动会导致开机联网缓慢，请注意，intel网卡 安装后向导配置是选择暂不联网，进入系统后继续设置

- 升级 OC 引导到 0.8.5
- 更新驱动适配 macos 13
- 集成 intel wifi驱动 2.2.0 预览版
- 集成 intel 蓝牙驱动至新版

2022-08-16

升级 OC 引导到 0.8.3，修正更新 BIOS 后卡EB的问题

2022-04-20

修正更新0.8后无法启动的问题，增加nvmefix驱动，缩小启动ui图标

2022-04-19

更新 OC 到 0.8.0 更新驱动到最新版本

2022-03-26

- 取消WG驱动注入(MacPro机型不需要该驱动)显卡跑分变高
- 引导默认隐藏工具，且不引导windows分区
- 加入gpu温度传感器，取消显卡注入信息
- SMBIOS信息改为主板注入（引导windows后显示正确主板信息）

2022-03-25

基础版本，基于 OC 0.7.9


