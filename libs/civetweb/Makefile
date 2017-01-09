include $(TOPDIR)/rules.mk

PKG_NAME:=civetweb
PKG_VERSION:=1.6
PKG_RELEASE:=0

PKG_SOURCE_URL:=http://intelight.s3.amazonaws.com/vendor
PKG_SOURCE:=intelight-civetweb-98404bcd4e79.tar.bz2
PKG_BUILD_DIR:=$(BUILD_DIR)/intelight-civetweb-98404bcd4e79

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/civetweb
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=embedded webserver
endef

$(eval $(call BuildPackage,civetweb))
