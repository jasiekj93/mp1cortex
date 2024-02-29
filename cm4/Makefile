# ------------------------------------------------
# @author Adrian Szczepanski
# @date 06-03-2023
# ------------------------------------------------

# Platform
# Uncomment if program platform must be diffrent than the solution
PLATFORM := ArmM4

# Target
target := cm4

# Directories
project_dir ?= ..
make_dir := $(project_dir)/make
external_dir := $(project_dir)/external

# Sources 
cxx_sources :=  \
$(wildcard *.cpp) \

c_sources := \
$(wildcard $(project_dir)/cube/CM4/Core/Src/*.c) \
$(wildcard $(project_dir)/cube/CM4/OPENAMP/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/libmetal/lib/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/libmetal/lib/system/generic/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/libmetal/lib/system/generic/template/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/open-amp/lib/remoteproc/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/open-amp/lib/rpmsg/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/virtual_driver/*.c) \
$(wildcard $(project_dir)/cube/Middlewares/Third_Party/OpenAMP/open-amp/lib/virtio/*.c) \
$(wildcard $(project_dir)/cube/Drivers/STM32MP1xx_HAL_Driver/Src/*.c) \
$(wildcard $(project_dir)/cube/Common/System/*.c) \

asm_sources := \
$(project_dir)/cube/CM4/Core/Startup/startup_stm32mp157dacx.s \

# Includes
cxx_includes := \
-I. \
-I$(project_dir)/cube/CM4/OPENAMP \
-I$(project_dir)/cube/CM4/Core/Inc \
-I$(project_dir)/cube/Middlewares/Third_Party/OpenAMP/open-amp/lib/include \
-I$(project_dir)/cube/Middlewares/Third_Party/OpenAMP/libmetal/lib/include \
-I$(project_dir)/cube/Drivers/STM32MP1xx_HAL_Driver/Inc \
-I$(project_dir)/cube/Drivers/STM32MP1xx_HAL_Driver/Inc/Legacy \
-I$(project_dir)/cube/Drivers/CMSIS/Device/ST/STM32MP1xx/Include \
-I$(project_dir)/cube/Middlewares/Third_Party/OpenAMP/virtual_driver \
-I$(project_dir)/cube/Drivers/CMSIS/Include \

# Defines
cxx_defs := \
-DDEBUG \
-DCORE_CM4 \
-DNO_ATOMIC_64_SUPPORT \
-DMETAL_INTERNAL \
-DMETAL_MAX_DEVICE_REGIONS=2 \
-DVIRTIO_SLAVE_ONLY \
-DUSE_HAL_DRIVER \
-DSTM32MP157Dxx 

# internal libraries
required_internal_libraries = \

# libraries
required_libraries = \

# external libraries
#	e.g. if include flag is '-I$(external_dir)/libFoo'
#	write 'libFoo'
external_library_include_path = \

external_library_flags = \

#	e.g. if link flag is '-L$(external_dir)/libFoo/lib'
#	write 'libFoo/lib'
external_library_paths = \

# Linker script
ldscript = $(project_dir)/cube/CM4/STM32MP157DACX_RAM.ld \

# Uncomment if gcc should be used for compilation *.c files
use_gcc_for_c_files := 1

# Uncomment if you want to add custom flags for gcc or g++
# custom_c_flags :=
# custom_cxx_flags :=

# Append rest of Makefile from template
include $(make_dir)/Program.mk