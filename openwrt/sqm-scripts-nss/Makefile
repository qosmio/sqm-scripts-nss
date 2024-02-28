include $(TOPDIR)/rules.mk

PKG_NAME:=sqm-scripts-nss
PKG_VERSION:=20240228
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/sqm-scripts-nss
  SECTION:=net
  DEPENDS:=+sqm-scripts +kmod-qca-nss-drv-qdisc +kmod-qca-nss-drv-igs
  PKGARCH:=all
  CATEGORY:=Base system
  TITLE:=SQM Scripts (QoS for NSS)
endef

define Package/sqm-scripts-nss/description
  Smart Queue Management Scripts for OpenWRT for use with NSS enabled builds.
endef

define Build/Configure
endef

define Build/Compile
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) $(CURDIR)/../../files/ $(PKG_BUILD_DIR)
endef

define Package/sqm-scripts-nss/install
	$(INSTALL_DIR) $(1)
	$(CP) $(PKG_BUILD_DIR)/files/* $(1)/
endef

$(eval $(call BuildPackage,sqm-scripts-nss))
