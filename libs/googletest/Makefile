include $(TOPDIR)/rules.mk

PKG_NAME:=googletest
PKG_VERSION:=1.8.0
PKG_RELEASE:=0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/google/googletest.git
PKG_SOURCE_VERSION:=release-1.8.0
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

CMAKE_OPTIONS += \
	-DBUILD_SHARED_LIBS=OFF \
	-Dgtest_build_tests=OFF \
	-Dgtest_build_samples=OFF \
	-Dgmock_build_tests=OFF

define Package/googletest
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=googletest and googlemock test libraries
endef

$(eval $(call BuildPackage,googletest))
