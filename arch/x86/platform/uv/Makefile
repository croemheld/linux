# SPDX-License-Identifier: GPL-2.0-only
obj-$(CONFIG_X86_UV)		+= tlb_uv.o bios_uv.o uv_irq.o uv_sysfs.o uv_time.o uv_nmi.o

ifeq ($(CONFIG_CLANG_STATIC_ANALYSIS),y)
CFLAGS_bios_uv.o += -O1
endif
