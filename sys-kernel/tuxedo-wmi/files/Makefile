ifneq ($(KERNELRELEASE),)
# kbuild part

obj-m := tuxedo-wmi.o

else
# development build

#KVERSION = $(shell uname -r)
KVERSION = $(shell readlink /usr/src/linux)
KDIR := /lib/modules/$(KVERSION)/build
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD)

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

install:
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install

endif
