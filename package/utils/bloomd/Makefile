include $(TOPDIR)/rules.mk

PKG_NAME:=bloomd
PKG_VERSION:=540

PKG_BUILD_DIR:=$(BUILD_DIR)/bloomd

include $(INCLUDE_DIR)/package.mk

define Package/bloomd
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Bloomd
	URL:=https://github.com/armon/bloomd
endef

define Package/bloomd/description
	Bloomd is a high-performance C server which is used to expose bloom filters
	and operations over them to networked clients. It uses a simple ASCII
	protocol which is human readable, and similar to memcached.
endef

include $(INCLUDE_DIR)/scons.bloomd.mk

define Package/bloomd/install
	$(INSTALL_DIR) $(1)/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/bloomd $(1)/bin/bloomd
endef

$(eval $(call BuildPackage,bloomd))
