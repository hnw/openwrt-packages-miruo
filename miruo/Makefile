include $(TOPDIR)/rules.mk

PKG_NAME:=miruo
PKG_VERSION:=0.9.6b
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/KLab/miruo/archive/
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_MD5SUM:=525f5a8d368cc975c3a230df9344d4c2

PKG_BUILD_PARALLEL:=1
PKG_INSTALL:=1
PKG_USE_MIPS16:=0

PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILES:=COPYING
PKG_MAINTAINER:=Yoshio HANAWA <for-openwrt@hnw.jp>

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Pretty-print TCP session monitor/analyzer
  URL:=https://github.com/KLab/miruo/
  DEPENDS:=+libpcap
endef

define Package/$(PKG_NAME)/description
  Network monitor/analyzer which prints packets on terminal in neat style.
  Packet data can also be read from a file saved by tcpdump(1).
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/sbin/miruo $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
