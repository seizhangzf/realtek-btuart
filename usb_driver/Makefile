ifneq ($(KERNELRELEASE),)
	obj-m := rtk_btusb.o
	rtk_btusb-y = rtk_coex.o rtk_misc.o rtk_bt.o
else
	PWD := $(shell pwd)
	KVER := $(shell uname -r)
	KDIR := /lib/modules/$(KVER)/build

all:
	$(MAKE) -C ${KERNEL_SRC} M=${M} ARCH=${ARCH} CROSS_COMPILE=${CROSS_COMPILE} modules

clean:
	rm -rf *.o *.mod.c *.mod.o *.ko *.symvers *.order *.a

endif
