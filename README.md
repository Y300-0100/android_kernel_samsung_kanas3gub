# android_samsung_kernel_sm-g355m
  Linux kernel release 3.x <http://kernel.org/>

1. How to Build Kernel:
	First navigate to your kernel source folder. In my case:

		cd /home/darkside/android/kernel/samsung/kanas3gub
		
	Than set path to your toolchain. In my case:
	
		export PATH=$PATH:/home/darkside/android/prebuilts/gcc/linux-x86/arm/arm-eabi-4.6/bin
		
	Than set arch and arm:
	
		export ARCH=arm
		export SUBARCH=arm
		export CROSS_COMPILE=arm-eabi-
		make kanas3g_hw02_defconfig
		make
		
	Your kernel will be in my case in:
	
		/home/darkside/android/kernel/samsung/kanas3gub/arch/arm/boot 
		(image = uncommpresed kernel zImage = commpresed kernel)
	
	
2. Allways before new build make clean:

		make mrproper
		
    
3. Kernel has enabled IO Schedulers, CPU Frequency scaling and selinux permissive which are disabled by default
