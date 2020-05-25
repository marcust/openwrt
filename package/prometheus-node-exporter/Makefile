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

PKG_NAME:=node-exporter
PKG_RELEASE:=1.0.0-rc.1
PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/node_exporter
  SECTION:=base
  CATEGORY:=Network
  TITLE:=Prometheus Node Exporter
  URL:=https://github.com/prometheus/node_exporter
endef

define Package/node_exporter/description
 This package contains the original node exporter.
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile/Default

endef
Build/Compile = $(Build/Compile/Default)

define Package/node_exporter/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,node_exporter))
