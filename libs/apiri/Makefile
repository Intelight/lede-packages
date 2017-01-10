#
# Copyright (C) 2011-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=apiri
PKG_VERSION:=2.01
PKG_RELEASE:=0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/Intelight/APIRI.git
PKG_SOURCE_VERSION:=7518c7d
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/libfio
  SECTION:=libs
  SUBMENU:=APIRI
  CATEGORY:=Libraries
  TITLE:=APIRI fio library
endef

define Package/libfpui
  SECTION:=libs
  SUBMENU:=APIRI
  CATEGORY:=Libraries
  TITLE:=APIRI fpui library
endef

define Package/libtod
  SECTION:=libs
  SUBMENU:=APIRI
  CATEGORY:=Libraries
  TITLE:=APIRI tod library
endef

define Build/Compile
	$(call Build/Compile/Default, api)
endef

define Build/Install
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/{lib,include}
	$(CP) $(PKG_BUILD_DIR)/fio/src/fioapi/libfio* $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/fio/src/fioapi/*.h $(1)/usr/include/
	$(CP) $(PKG_BUILD_DIR)/fpu/FrontPanelSystem/libfpui/libfpui* $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/fpu/FrontPanelSystem/libfpui/*.h $(1)/usr/include/
	$(CP) $(PKG_BUILD_DIR)/tod/src/libtod* $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/tod/src/*.h $(1)/usr/include/
endef

define Package/libfio/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/fio/src/fioapi/libfio*so* $(1)/usr/lib/
endef

define Package/libfpui/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/fpu/FrontPanelSystem/libfpui/libfpui*so* $(1)/usr/lib/
endef

define Package/libtod/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_BUILD_DIR)/tod/src/libtod*so* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libfio))
$(eval $(call BuildPackage,libfpui))
$(eval $(call BuildPackage,libtod))
