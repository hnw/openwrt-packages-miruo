# openwrt-packages-miruo [![Build Status](https://secure.travis-ci.org/hnw/openwrt-packages-miruo.svg?branch=master)](https://travis-ci.org/hnw/openwrt-packages-miruo)

This is [miruo](https://github.com/KLab/miruo/) package for OpenWrt, tested on OpenWrt 15.05.1 / LEDE 17.01.4.

# How to install binary package

See [hnw/openwrt-packages](https://github.com/hnw/openwrt-packages).

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot/SDK environment:

```
$ cp feeds.conf.default feeds.conf # if needed
$ echo 'src-git hnw_miruo https://github.com/hnw/openwrt-packages-miruo.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install miruo
$ make defconfig
$ make package/toolchain/compile
$ make package/miruo/compile
```
