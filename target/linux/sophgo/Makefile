# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

BOARD:=sophgo
BOARDNAME:=Sophgo
FEATURES:=ext4 audio usb usbgadget display gpio fpu pci pcie rootfs-part boot-part squashfs
SUBTARGETS:=cv186ah bm1688

KERNEL_PATCHVER=5.10

define Target/Description
	Build firmware image for Sophgo SoC devices.
endef

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += partx-utils e2fsprogs mkf2fs kmod-gpio-button-hotplug

KERNELNAME:=Image dtbs

$(eval $(call BuildTarget))
