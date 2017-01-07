#
# Copyright (C) 2007-2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=protobuf-cmake
PKG_VERSION:=3.0.2
PKG_RELEASE:=0

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/google/protobuf.git
PKG_SOURCE_VERSION:=v3.0.2
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

# The protobuf top level CMakeLists.txt is in the cmake subdir
CMAKE_SOURCE_DIR=$(PKG_BUILD_DIR)/cmake

define Package/protobuf-cmake
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=A structured data encoding library (cmake build)
  URL:=http://code.google.com/p/protobuf/
  DEPENDS:=+zlib
endef

define Package/protobuf-cmake/description
 Protocol Buffers are a way of encoding structured data in an efficient
 yet extensible format. Google uses Protocol Buffers for almost all
 of its internal RPC protocols and file formats.
endef

CMAKE_OPTIONS += \
	-DBUILD_SHARED_LIBS=OFF \
	-Dprotobuf_BUILD_TESTS=OFF \
	-Dprotobuf_WITH_ZLIB_DEFAULT=ON

$(eval $(call BuildPackage,protobuf-cmake))
