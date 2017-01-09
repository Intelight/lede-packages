include $(TOPDIR)/rules.mk

PKG_NAME:=snmp-pp
PKG_VERSION:=2.6
PKG_RELEASE:=0

PKG_SOURCE_URL:=http://intelight.s3.amazonaws.com/vendor
PKG_SOURCE:=intelight-snmp-0b0f75e41b09.tar.bz2
PKG_BUILD_DIR:=$(BUILD_DIR)/intelight-snmp-0b0f75e41b09

CMAKE_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/snmp-pp
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=SNMP++ 2.6 For HP UNIX Source Code
endef

$(eval $(call BuildPackage,snmp-pp))
