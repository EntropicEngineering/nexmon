# SPDX-License-Identifier: ISC
#
# Makefile fragment for Broadcom 802.11 Networking Device Driver
#
# Copyright (c) 2010 Broadcom Corporation
#

ccflags-y += \
	-I$(NEXMON_ROOT)/patches/driver/brcmfmac_5.15.y-nexmon	\
	-I$(NEXMON_ROOT)/patches/driver/brcmfmac_5.15.y-nexmon/include \
	-DDEBUG

MODULENAME = brcmfmac-monitor-mode

obj-$(CONFIG_BRCMFMAC) += $(MODULENAME).o
$(MODULENAME)-objs += \
		cfg80211.o \
		chip.o \
		fwil.o \
		fweh.o \
		p2p.o \
		proto.o \
		common.o \
		core.o \
		firmware.o \
		feature.o \
		btcoex.o \
		vendor.o \
		pno.o \
		xtlv.o
$(MODULENAME)-$(CONFIG_BRCMFMAC_PROTO_BCDC) += \
		bcdc.o \
		fwsignal.o
$(MODULENAME)-$(CONFIG_BRCMFMAC_PROTO_MSGBUF) += \
		commonring.o \
		flowring.o \
		msgbuf.o
$(MODULENAME)-$(CONFIG_BRCMFMAC_SDIO) += \
		sdio.o \
		bcmsdh.o
$(MODULENAME)-$(CONFIG_BRCMFMAC_USB) += \
		usb.o
$(MODULENAME)-$(CONFIG_BRCMFMAC_PCIE) += \
		pcie.o
$(MODULENAME)-$(CONFIG_BRCMDBG) += \
		debug.o
$(MODULENAME)-$(CONFIG_BRCM_TRACING) += \
		tracepoint.o
$(MODULENAME)-$(CONFIG_OF) += \
		of.o
$(MODULENAME)-$(CONFIG_DMI) += \
		dmi.o
