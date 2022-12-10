INC_INCPATH := $(KBUILD_EXTMOD)/include

LINUXINCLUDE := \
    -I$(INC_INCPATH)/trace \
	-I$(KBUILD_EXTMOD)/drivers/gpu/drm/i915 \
    -I$(KBUILD_EXTMOD)/drivers/gpu/drm/i915/gvt \
    $(LINUXINCLUDE)

obj-m		+= drivers/gpu/drm/i915/

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(shell pwd) -j4 modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(shell pwd) clean
