include $(TOPDIR)/rules.mk

PKG_NAME:=lua-intf
PKG_VERSION:=1.0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/SteveKChiu/lua-intf.git
PKG_SOURCE_VERSION:=0ff4fc9
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/lua-intf
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=lua-intf is a binding between C++11 and Lua
endef

define Build/Configure
endef

define Build/Compile
endef

define Build/InstallDev
        $(INSTALL_DIR) $(STAGING_DIR)/usr/include/
	$(CP) -r $(PKG_BUILD_DIR)/LuaIntf $(STAGING_DIR)/usr/include/
endef

$(eval $(call BuildPackage,lua-intf))
