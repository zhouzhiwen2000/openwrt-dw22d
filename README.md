# openwrt-dw22d
add support for dw22d (image builder)
利用ImageBuilder将机型支持代码与OpenWrt官方二进制程序合并生成固件
git clone https://github.com/zhouzhiwen2000/openwrt-dw22d.git
cd openwrt-dw22d/ImageBuilder
# 下载ImageBuilder和SDK
ImageBuilder:https://archive.openwrt.org/barrier_breaker/14.07/ramips/mt7620a/OpenWrt-ImageBuilder-ramips_mt7620a-for-linux-x86_64.tar.bz2
SDK:https://archive.openwrt.org/barrier_breaker/14.07/ramips/mt7620a/OpenWrt-SDK-ramips-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
# 解压ImageBuilder和SDK
tar jxvf OpenWrt-ImageBuilder-ramips_mt7620a-for-linux-x86_64.tar.bz2
tar jxvf OpenWrt-SDK-ramips-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
  
# 生成固件：
make DW22D FEEDS=1 RALINK=1

# FEEDS=1 表示包含项目network-feeds 的功能在内
# RALINK=1 表示包含5G驱动在固件中
Thanks to the project:rssnsj/openwrt-hc5x61/.
