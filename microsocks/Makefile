include $(TOPDIR)/rules.mk

PKG_NAME:=microsocks
PKG_VERSION=1.0
PKG_RELEASE:=1

PKG_MAINTAINER:=lean
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/rofl0r/microsocks.git
PKG_MIRROR_HASH:=b13f4d69c568d13d68021cc4a1aff9410a3e3767b562656b3e06108c819d72e2
PKG_SOURCE_VERSION:=5795a84c4fbd61685690a8cd6d43969efc083614

PKG_SOURCE_SUBDIR:=$(PKG_NAME)
PKG_SOURCE:=$(PKG_NAME).$(PKG_VERSION).$(PKG_RELEASE).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/microsocks
	SECTION:=net
	CATEGORY:=Network
	TITLE:=microsocks for OpenWRT
	DEPENDS:=
endef

define Package/microsocks/description
	microsocks is a Tiny Proxy in C.
endef

define Package/microsocks/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/microsocks $(1)/usr/bin/microsocks
endef

$(eval $(call BuildPackage,microsocks))
