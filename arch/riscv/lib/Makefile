# SPDX-License-Identifier: GPL-2.0-only
lib-y			+= delay.o
lib-$(CONFIG_MMU)	+= uaccess.o
lib-$(CONFIG_64BIT)	+= tishift.o
lib-$(CONFIG_CC_OPTIMIZE_FOR_PERFORMANCE) += string.o

# string.o implements standard library functions like memset/memcpy etc.
# Use -ffreestanding to ensure that the compiler does not try to "optimize"
# them into calls to themselves.
CFLAGS_string.o := -ffreestanding

obj-$(CONFIG_FUNCTION_ERROR_INJECTION) += error-inject.o
