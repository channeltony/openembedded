ifneq ($(KERNELRELEASE),)
pwc-objs        := pwc-if.o pwc-misc.o pwc-ctrl.o pwc-v4l.o pwc-uncompress.o \
		   pwc-dec1.o pwc-dec23.o pwc-kiara.o pwc-timon.o

obj-m	+= pwc.o

else
KDIR	:= /lib/modules/$(shell uname -r)/build
PWD	:= $(shell pwd)

default modules:
	$(MAKE) -C $(KDIR) SUBDIRS=$(PWD) modules
endif
