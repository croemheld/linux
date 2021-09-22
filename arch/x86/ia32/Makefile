# SPDX-License-Identifier: GPL-2.0-only
#
# Makefile for the ia32 kernel emulation subsystem.
#

obj-$(CONFIG_IA32_EMULATION) := sys_ia32.o ia32_signal.o

ifeq ($(CONFIG_CLANG_STATIC_ANALYSIS),y)
CFLAGS_sys_ia32.o += -O1
CFLAGS_ia32_signal.o += -O1
endif

obj-$(CONFIG_IA32_AOUT) += ia32_aout.o

audit-class-$(CONFIG_AUDIT) := audit.o
obj-$(CONFIG_IA32_EMULATION) += $(audit-class-y)
