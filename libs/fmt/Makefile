include $(TOPDIR)/rules.mk

PKG_NAME:=fmt
PKG_VERSION:=3.0.1
PKG_RELEASE:=0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/fmtlib/fmt.git
PKG_SOURCE_VERSION:=3.0.1
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

CMAKE_OPTIONS += \
	-DFMT_DOC=OFF \
	-DFMT_TEST=OFF

define Package/fmt
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=fmt is an open-source formatting library for C++
endef

$(eval $(call BuildPackage,fmt))

