#
# Copyright (C) 2015 John Crispin <blogic@openwrt.org>
#
# This is free software, licensed under the GPL 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mtk-linkit-webui
PKG_VERSION:=0.1.2
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/MediaTek-Labs/linkit-smart-7688-webUI.git
PKG_MIRROR_HASH:=682373593ab62ab4cd556fab6c051cec985bcea655b8759dac8c0f3c1319f237
PKG_SOURCE_DATE:=2015-07-07
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=3676d579f7fc56dd9b07f2f75233acfbced7f032
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

include $(INCLUDE_DIR)/package.mk

define Package/mtk-linkit-webui
  SECTION:=ralink
  CATEGORY:=Ralink SDK
  TITLE:=LinkIt Smart 7688 Webui
  DEPENDS:=@TARGET_ramips_mt76x8_DEVICE_mediatek_linkit-smart-7688
#   HIDDEN:=1
endef

define Build/Configure
	true
endef

define Build/Compile
	true
endef

define Package/mtk-linkit-webui/install
	$(INSTALL_DIR) $(1)/www/build
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/build/* $(1)/www/build/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/zh-*.html $(1)/www/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app/index.html $(1)/www/index_7688.html
endef

$(eval $(call BuildPackage,mtk-linkit-webui))
