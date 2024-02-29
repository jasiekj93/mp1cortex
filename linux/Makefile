# ------------------------------------------------
# @author Adrian Szczepanski
# @date 21-02-2024
# ------------------------------------------------

# Directories
project_dir ?= ..
make_dir := $(project_dir)/make

linux_root := /home/aszczepanski/stm32mp1/developer/stm32mp1-openstlinux-6.1-yocto-mickledore-mp1-v23.06.21/sources/arm-ostl-linux-gnueabi/linux-stm32mp-6.1.28-stm32mp-r1-r0
sdk_enviroment := /home/aszczepanski/stm32mp1/developer/sdk/environment-setup-cortexa7t2hf-neon-vfpv4-ostl-linux-gnueabi

hostname := root@192.168.7.1
kernel_version := 6.1.28

device_tree_source := \
$(project_dir)/cube/CA7/DeviceTree/mp1cortexm4/kernel/stm32mp157d-mp1cortexm4-mx.dts

device_tree_board_name := stm32mp157d-dk1.dtb

# Append rest of Makefile from template
include $(make_dir)/Linux.mk