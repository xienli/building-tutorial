################################################################################

1-1. How to Build kernel
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-eabi-4.8
		 - linaro-gcc latest or older
		 - ubertc
		 - sabermod,etc
		
	- edit Makefile or export your path compiler
		edit "CROSS_COMPILE" line on with where you save compile
		or you can just export path
		$ export CROSS_COMPILE=(compiler path)
		$ export ARCH=arm
		$ mkdir out
		$ make -C $(pwd) O=out msm8916_sec_defconfig VARIANT_DEFCONFIG=msm8916_sec_fortunave3g_eur_defconfig SELINUX_DEFCONFIG=selinux_defconfig TIMA_DEFCONFIG=tima8916_defconfig
		$ make -C $(pwd) O=out
		$ cp out/arch/arm/boot/zImage arch/arm/boot/zImage

1-2. excute build command after edit Toolchain path.
          ./build_kernel.sh

2. Output files
	- Kernel : out/arch/arm/boot/zImage
	- module : out/drivers/*/*.ko

3. How to Clean	
		$ cd out
		$ make clean

################################################################################
