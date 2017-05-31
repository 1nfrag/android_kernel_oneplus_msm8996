dtb-$(CONFIG_ARCH_MSM8996) += msm8996-v3-pmi8996-mtp_15801.dtb \
    msm8996pro-pmi8996-mtp_15811.dtb

ifeq ($(CONFIG_PRODUCT_LE_X2),y)
dtb-$(CONFIG_ARCH_MSM8996) += \
	msm8996-v2-pmi8994-le_x2-evt.dtb \
	msm8996-v2-pmi8994-le_x2-dvt1.dtb \
	msm8996-v3-pmi8994-le_x2-evt.dtb \
	msm8996-v3-pmi8994-le_x2-dvt1.dtb \
	msm8996-v3-pmi8994-le_x2-dvt1.1.dtb \
	msm8996-v3-pmi8996-le_x2-evt.dtb \
	msm8996-v3-pmi8996-le_x2-dvt1.dtb \
	msm8996-v3-pmi8996-le_x2-dvt1.1.dtb \
	msm8996-v3-pmi8994-le_x2_na-evt.dtb \
	msm8996-v3-pmi8994-le_x2_na-dvt1.dtb \
	msm8996-v3-pmi8996-le_x2_na-evt.dtb \
	msm8996-v3-pmi8996-le_x2_na-dvt1.dtb \
	msm8996-v3-pmi8994-le_x2-dvt2.dtb \
	msm8996-v3-pmi8996-le_x2-dvt2.dtb \
	msm8996-v3-pmi8994-le_x2_na-dvt1.1.dtb \
	msm8996-v3-pmi8996-le_x2_na-dvt1.1.dtb \
	msm8996-v3-pmi8994-le_x2-pvt.dtb \
	msm8996-v3-pmi8996-le_x2-pvt.dtb \
	msm8996-v3-pmi8994-le_x2_na-dvt2.dtb \
	msm8996-v3-pmi8996-le_x2_na-dvt2.dtb \
	msm8996-v3-pmi8996-le_x2_na-pvt.dtb \
	msm8996-v3-pmi8994-le_x2_na-pvt.dtb \
	msm8996pro-v3-pmi8996-le_x2-pvt.dtb
endif

ifeq ($(CONFIG_PRODUCT_LE_ZL1),y)
dtb-$(CONFIG_ARCH_MSM8996) += \
	msm8996-v3-pmi8996-le_zl1-evt.dtb \
	msm8996-v3-pmi8996-le_zl1-dvt1.dtb \
	msm8996pro-pmi8996-le_zl1-dvt1.dtb \
	msm8996pro-pmi8996-le_zl1-na.dtb \
	msm8996pro-pmi8996-le_zl1-pvt.dtb
endif

dtb-$(CONFIG_ARCH_MSM8996) += msm8996-v2-pmi8994-cdp.dtb \
	msm8996-v2-pmi8994-mtp.dtb \
	msm8996-v3-pmi8994-mtp.dtb \
	msm8996-v3-pmi8996-mtp.dtb \
	msm8996pro-pmi8994-mtp.dtb \
	msm8996pro-pmi8996-mtp.dtb \
	msm8996pro-v1.1-pmi8994-mtp.dtb \
	msm8996pro-v1.1-pmi8996-mtp.dtb \
	msm8996-v3.0-pmi8994-mtp.dtb \
	msm8996-v3.0-pmi8996-mtp.dtb


ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/,$(dtb-y))
endif
clean-files := *.dtb
