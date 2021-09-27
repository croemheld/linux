# SPDX-License-Identifier: GPL-2.0
ccflags-$(CONFIG_COMEDI_DEBUG)		:= -DDEBUG

comedi-y				:= comedi_fops.o range.o drivers.o \
					   comedi_buf.o
comedi-$(CONFIG_PROC_FS)		+= proc.o
comedi-$(CONFIG_COMPAT)			+= comedi_compat32.o

ifeq ($(CONFIG_CLANG_STATIC_ANALYSIS),y)
CFLAGS_comedi_compat32.o += -O1
endif

obj-$(CONFIG_COMEDI_PCI_DRIVERS)	+= comedi_pci.o
obj-$(CONFIG_COMEDI_PCMCIA_DRIVERS)	+= comedi_pcmcia.o
obj-$(CONFIG_COMEDI_USB_DRIVERS)	+= comedi_usb.o

obj-$(CONFIG_COMEDI)			+= comedi.o

obj-$(CONFIG_COMEDI)			+= kcomedilib/
obj-$(CONFIG_COMEDI)			+= drivers/
