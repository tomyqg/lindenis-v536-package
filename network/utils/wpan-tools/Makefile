#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=wpan-tools
PKG_VERSION:=0.5

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=http://wpan.cakelab.org/releases/
PKG_MD5SUM:=6226df405a98c13ec41bf4d1f0777d6b

include $(BUILD_DIR)/package.mk

define Package/wpan-tools
  SECTION:=net
  CATEGORY:=Network
  TITLE:=cfg802154 interface configuration utility
  URL:=http://wpan.cakelab.org/
  DEPENDS:= +libnl
endef

define Build/Configure
  $(call Build/Configure/Default)
endef

define Package/wpan-tools/install
	$(INSTALL_DIR) $(1)/usr/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/src/iwpan $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,wpan-tools))
