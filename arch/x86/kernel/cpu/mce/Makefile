# SPDX-License-Identifier: GPL-2.0
obj-y				=  core.o severity.o genpool.o

ifeq ($(CONFIG_CLANG_STATIC_ANALYSIS),y)
CFLAGS_core.o += -O1
CFLAGS_therm_throt.o += -O1
endif

obj-$(CONFIG_X86_ANCIENT_MCE)	+= winchip.o p5.o
obj-$(CONFIG_X86_MCE_INTEL)	+= intel.o
obj-$(CONFIG_X86_MCE_AMD)	+= amd.o
obj-$(CONFIG_X86_MCE_THRESHOLD) += threshold.o

mce-inject-y			:= inject.o
obj-$(CONFIG_X86_MCE_INJECT)	+= mce-inject.o

obj-$(CONFIG_X86_THERMAL_VECTOR) += therm_throt.o

obj-$(CONFIG_ACPI_APEI)		+= apei.o

obj-$(CONFIG_X86_MCELOG_LEGACY)	+= dev-mcelog.o
