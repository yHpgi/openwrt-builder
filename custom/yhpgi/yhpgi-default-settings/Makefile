#
# Copyright (C) 2016-2024 GitHub 
#
# This is free software, licensed under the GNU General Public License v2 only.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=yhpgi-default-settings
PKG_RELEASE:=2

PKG_LICENSE:=GPL-2.0-only

include $(INCLUDE_DIR)/package.mk

define Package/yhpgi-default-settings
  SECTION:=luci
  CATEGORY:=LuCI
  TITLE:=yhpgi Default Settings
  DEPENDS:=+luci +luci-base +block-mount +kmod-fs-ext4 +e2fsprogs +usbutils +kmod-usb-storage
  PKGARCH:=all
endef

define Build/Compile
endef

define Package/yhpgi-default-settings/install
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/88-default-settings $(1)/etc/uci-defaults/
endef

$(eval $(call BuildPackage,yhpgi-default-settings))
