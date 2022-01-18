# Copyright (C) 2022 OpenWrt.org

include $(TOPDIR)/rules.mk

PKG_NAME:=cgi-ubus
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Sergey Ponomarev <stokito@gmail.com>
PKG_LICENSE:=ISC
PKG_SOURCE_URL:=https://github.com/yurt-page/cgi-ubus

include $(INCLUDE_DIR)/package.mk

define Package/cgi-ubus
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Web Servers/Proxies
  TITLE:=CGI to submit to UBUS
  DEPENDS:=+ubus
  PKGARCH:=all
endef

define Package/cgi-ubus/description
  CGI to submit to UBUS
endef

define Build/Compile
endef

define Package/cgi-ubus/install
	$(INSTALL_DIR) $(1)/usr/libexec $(1)/www/cgi-bin/
	$(INSTALL_BIN) ./files/usr/libexec/ubus.sh $(1)/usr/libexec/
	$(LN) ../../usr/libexec/ubus.sh $(1)/www/cgi-bin/
endef

$(eval $(call BuildPackage,cgi-ubus))
