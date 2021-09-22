# SPDX-License-Identifier: GPL-2.0-only
#
# Build rules for the FPU support code:
#

obj-y				+= init.o bugs.o core.o regset.o signal.o xstate.o

ifeq ($(CONFIG_CLANG_STATIC_ANALYSIS),y)
CFLAGS_signal.o += -O1
endif
