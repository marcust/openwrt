#
# Copyright (C) 2007-2016 OpenWrt.org
# Copyright (C) 2010 Vertical Communications
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk
include $(INCLUDE_DIR)/version.mk
include $(INCLUDE_DIR)/feeds.mk

PKG_NAME:=speedtest
PKG_RELEASE:=1.0.0
PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/speedtest
  SECTION:=base
  CATEGORY:=Network
  TITLE:=Command Line SpeedTest Utility
  URL:=https://www.speedtest.net/de/apps/cli
endef

define Package/speedtest/description
 This package contains a command line speedtest client.
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile/Default

endef
Build/Compile = $(Build/Compile/Default)

define Package/speedtest/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,speedtest))
