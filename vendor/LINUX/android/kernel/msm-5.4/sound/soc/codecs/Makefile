ifneq ($(KERNELRELEASE),)
obj-m := acm8625s.o
else
KDIR := /lib/modules/$(shell uname -r)/build    # KDIR := [path-to-target-kernel-source] if cross compiling
all:
	make -C $(KDIR) M=$(PWD) modules
clean:
	make -C $(KDIR) M=$(PWD) clean
endif	