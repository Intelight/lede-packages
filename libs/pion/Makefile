include $(TOPDIR)/rules.mk

PKG_NAME:=pion
PKG_VERSION:=4.0.11
PKG_RELEASE:=0

PKG_SOURCE_URL:=http://intelight.s3.amazonaws.com/vendor
PKG_SOURCE:=intelight-old-pion-net-08aa24212b04.tar.bz2
PKG_BUILD_DIR:=$(BUILD_DIR)/intelight-old-pion-net-08aa24212b04

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/pion
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=pion network library based on boost
endef

$(eval $(call BuildPackage,pion))
