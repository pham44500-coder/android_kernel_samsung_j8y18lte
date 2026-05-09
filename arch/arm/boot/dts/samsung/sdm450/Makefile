# Samsung SDM450 Project

dtb-$(CONFIG_MACH_J8PLTE_EUR_OPEN) += sdm450-sec-j8plte_eur_open-r00.dtb \
					sdm450-sec-j8plte_eur_open-r01.dtb \
					sdm450-sec-j8plte_eur_open-r02.dtb \
					sdm450-sec-j8plte_eur_open-r03.dtb \
					sdm450-sec-j8plte_eur_open-r04.dtb

dtb-$(CONFIG_MACH_J8PLTE_CIS_SER) += sdm450-sec-j8plte_cis_ser-r00.dtb \
					sdm450-sec-j8plte_cis_ser-r01.dtb \
					sdm450-sec-j8plte_cis_ser-r02.dtb \
					sdm450-sec-j8plte_cis_ser-r03.dtb \
					sdm450-sec-j8plte_cis_ser-r04.dtb

dtb-$(CONFIG_MACH_J8PLTE_SEA_OPEN) += sdm450-sec-j8plte_eur_open-r00.dtb \
					sdm450-sec-j8plte_eur_open-r01.dtb \
					sdm450-sec-j8plte_eur_open-r02.dtb \
					sdm450-sec-j8plte_eur_open-r03.dtb \
					sdm450-sec-j8plte_eur_open-r04.dtb

dtb-$(CONFIG_MACH_J8PLTE_CHN_OPEN) += sdm450-sec-j8plte_chn_open-r00.dtb \
					sdm450-sec-j8plte_chn_open-r01.dtb \
					sdm450-sec-j8plte_chn_open-r02.dtb \
					sdm450-sec-j8plte_chn_open-r03.dtb \
					sdm450-sec-j8plte_chn_open-r04.dtb

dtb-$(CONFIG_MACH_J8PLTE_KOR_KTT) += sdm450-sec-j8plte_kor_ktt-r00.dtb \
					sdm450-sec-j8plte_kor_ktt-r01.dtb \
					sdm450-sec-j8plte_kor_ktt-r02.dtb \
					sdm450-sec-j8plte_kor_ktt-r03.dtb \
					sdm450-sec-j8plte_kor_ktt-r04.dtb

dtb-$(CONFIG_MACH_J8PLTE_LTN_OPEN) += sdm450-sec-j8plte_ltn_open-r03.dtb \
                                        sdm450-sec-j8plte_ltn_open-r04.dtb

dtb-$(CONFIG_MACH_J8Y18LTE_SWA_INS) += sdm450-sec-j8y18lte_swa_ins-r00.dtb \
					sdm450-sec-j8y18lte_swa_ins-r01.dtb \
					sdm450-sec-j8y18lte_swa_ins-r02.dtb \
					sdm450-sec-j8y18lte_swa_ins-r03.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(dtb-y))
endif
clean-files := *.dtb *.reserve.dts
