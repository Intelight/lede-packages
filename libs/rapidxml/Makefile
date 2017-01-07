include $(TOPDIR)/rules.mk

PKG_NAME:=rapidxml
PKG_VERSION:=1.13

PKG_SOURCE_URL:=@SF/$(PKG_NAME)
PKG_SOURCE_VERSION:=d74d360
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).zip
PKG_MD5SUM:=7b4b42c9331c90aded23bb55dc725d6a

include $(INCLUDE_DIR)/package.mk

define Package/rapidxml
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=rapidxml library
endef

define Build/Configure
endef

define Build/Compile
endef

define Build/InstallDev
        $(INSTALL_DIR) $(STAGING_DIR)/usr/include/
	$(CP) $(PKG_BUILD_DIR)/*.hpp $(STAGING_DIR)/usr/include/
endef

$(eval $(call BuildPackage,rapidxml))
