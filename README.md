# Hackintosh-12700KF-B660M-MORTAR-6600XT

适用于 12700KF + B660M迫击炮 DDR4 + 6600XT 黑苹果引导文件

基于 OpenCore 0.7.9 版本，机型 MacPro 7,1，系统 MacOS 12.3

本 EFI 参考其他基于 12代 引导与查阅资料，去除不必要的驱动并更新到最新版本

USB定制在15个端口内，保留内置 AX201 蓝牙与内置 JUSB-1 接口

# 注意事项

本引导适用于 B660M 迫击炮主板，主板BIOS需一下设置


禁用：
Onboard CNVi Module Control-Disable Integrated
快速开机
Intel VT-D
CFG锁定
Speed Select Technology

开启：
Re-Size BAR Support
SR-IOV Support
电源 / err ready

注入 AirportBrcmFixup 使943602cs达到 1300M 连接速率但是需要关闭 节能 - 唤醒已供网络访问

# 本机配置

| 配置        | 型号                               |
|-----------|----------------------------------|
| CPU       | intel i7 12700KF                 |
| 主板        | MSI MAG BB60M MORTAR WiF DDR4    |
| 显卡        | 蓝宝石 AMD Radeon RX 6600 8G OC 超白金 |
| 内存        | 海盗船 3200MHz 16G * 2              |
| SSD       | 铠侠 RC20 1T NVME SSD              |
| 机箱        | 屌丝伯 D30 前面板 1USB 1 TYPE-C(USB转)  |
| 电源        | 鑫谷750w ATX                       |
| CPU 风扇    | 利民 PA120 SE                      |
| WiFi + 蓝牙 | BCM94360CD (PCI+USB转接卡)          |


# 使用情况：
cpu正常，节能三项，睡眠正常，唤醒正常，usb2/3正常，声卡正常，wifi正常(禁用自带蓝牙和网卡)


# 更新记录

2022-03-25
基础版本，基于 OC 0.7.9


