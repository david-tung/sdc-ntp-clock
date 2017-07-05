#
# Copyright (C) 2015 John Crispin <blogic@openwrt.org>
#
# This is free software, licensed under the GPL 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=sdc-ntp-clock
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/sdc-ntp-clock
  TITLE:=SDC Ntp Clock
  DEPENDS:=@TARGET_ramips_mt7688_LinkIt7688 \
  			+ntpd
  HIDDEN:=1
  CATEGORY:=Base system
  DEFAULT:=y
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
	true
endef

define Build/Compile
	true
endef

define Package/sdc-ntp-clock/extra_provides
	echo 'libnetsnmp.so.30'; \
	echo 'libnetsnmpagent.so.30'; \
	echo 'libnetsnmpmibs.so.30'; \
	echo 'libnetsnmptrapd.so.30';
endef

define Package/sdc-ntp-clock/install
	$(CP) -fpR ./files/* $(1)
endef

$(eval $(call BuildPackage,sdc-ntp-clock))
