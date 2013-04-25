___________________________________________________________________________________________________________

                                    CROSS COMPILER TOOLCHAINS - README
___________________________________________________________________________________________________________


This repo contains some of the latest cross compiler toolchains I've built for Android kernel development,
it contains the following:

* Stable builds *
- "Linaro GCC 4.7.3-2013.04 Toolchains" subfolder contains the toolchains that include Linaro GCC 4.7-2013.04 (4.7.3)
  and Linaro GDB 7.5-2012.12
- "Linaro GCC 4.6.4-2013.04 Toolchains" subfolder contains the toolchains that include Linaro GCC 4.6-2013.04 (4.6.4)
  and Linaro GDB 7.5-2012.12

* Experimental builds *
- Linaro GCC 4.8.1-2013.04 Toolchains subfolder contains the toolchains that include Linaro GCC 4.8-2013.04 (4.8.1)
  and Linaro GDB 7.5-2012.12

Note: The GCC 4.8 toolchains could cause incompatibility problems with some kernels (including I9001 kernel)


You can find other zipped toolchain builds on my Mediafire folder, please take a look at the original thread on
XDA Developers forum at this link:
       http://forum.xda-developers.com/showthread.php?t=2098133


- The toolchains with "arm-unknown-linux-gnueabi" prefix are built for generic Cortex-A cpu and configured with
similar settings to those of the latest Linaro toolchains
- The toolchains with "arm-cortex_a8-linux-gnueabi" prefix are optimized for Cortex-A8 cpu with Neon technology
support (like Qualcomm Snapdragon Scorpion cpu mounted on Samsung S Plus I9001)

I hope you find them useful...
Let me know.
Thanks!

Christopher


These are the details on each toolchain currently available on this repo


___________________________________________________________________________________________________________

                      TOOLCHAIN arm-unknown-linux-gnueabi-linaro_4.8-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Generic ARM settings (inspired by latest Linaro builds) for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU=""
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="vfpv3-d16"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="thumb"
    CT_ARCH_ARM_MODE_THUMB=y

- Linux Kernel 3.0.72
- GCC Linaro-4.8-2013.04 (4.8.1)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-cortex_a8-linux-gnueabi-linaro_4.8-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Cortex-A8 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a8"
    CT_ARCH_TUNE="cortex-a8"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.0.72
- GCC Linaro-4.8-2013.04 (4.8.1)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                   TOOLCHAIN arm-unknown-linux-gnueabi-linaro_4.7.3-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Generic ARM settings (inspired by latest Linaro builds) for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU=""
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="vfpv3-d16"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="thumb"
    CT_ARCH_ARM_MODE_THUMB=y

- Linux Kernel 3.0.72
- GCC Linaro-4.7-2013.04 (4.7.3)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                  TOOLCHAIN arm-cortex_a8-linux-gnueabi-linaro_4.7.3-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Cortex-A8 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a8"
    CT_ARCH_TUNE="cortex-a8"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.0.72
- GCC Linaro-4.7-2013.04 (4.7.3)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                    TOOLCHAIN arm-unknown-linux-gnueabi-linaro_4.6.4-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Generic ARM settings (inspired by latest Linaro builds) for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU=""
    CT_ARCH_TUNE="cortex-a9"
    CT_ARCH_FPU="vfpv3-d16"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="thumb"
    CT_ARCH_ARM_MODE_THUMB=y

- Linux Kernel 3.0.72
- GCC Linaro-4.6-2013.04 (4.6.4)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"

___________________________________________________________________________________________________________

                  TOOLCHAIN arm-cortex_a8-linux-gnueabi-linaro_4.6.4-2013.04

- Built using latest crosstool-ng toolchain builder (hg+default-0fc56e62cecf)
- Cortex-A8 specific settings for target architecture and target optimizations:
    CT_ARCH_ARCH="armv7-a"
    CT_ARCH_CPU="cortex-a8"
    CT_ARCH_TUNE="cortex-a8"
    CT_ARCH_FPU="neon"
    CT_ARCH_FLOAT_SOFTFP=y
    CT_ARCH_FLOAT="softfp"
    CT_ARCH_ARM_MODE="arm"
    CT_ARCH_ARM_MODE_ARM=y

- Linux Kernel 3.0.72
- GCC Linaro-4.6-2013.04 (4.6.4)
- Binutils 2.23.1
- EGLibc 2.17
- DMalloc 5.5.2
- Duma 2.5.15
- GDB Linaro-7.5-2012.12-1
- LTrace 0.5.3
- STrace 4.6
- GMP 5.0.2
- MPFR 3.1.0
- PPL 0.11.2
- CLOOG 0.15.11
- MPC 0.9
- LibElf 0.8.13
- Multilib support
- Alias "arm-gnueabi-"
