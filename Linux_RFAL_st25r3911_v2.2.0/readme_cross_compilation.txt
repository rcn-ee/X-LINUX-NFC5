How to build on Ubuntu 16.04 (and above) for STM32MP157C-DK2

1. Install cmake for Linux (use below command)

    $ sudo apt-get install cmake

2. Install cross-compilation toolchain & set environment to Enable the SDK (follow below link)
  https://wiki.st.com/stm32mpu/wiki/Getting_started/STM32MP1_boards/STM32MP157C-DK2/Develop_on_Arm%C2%AE_Cortex%C2%AE-A7/Install_the_SDK

3. Enter the build directory in the Demo application source code
  $ cd Linux_RFAL_st25r3911_v2.0.4/linux_demo/build

4. RUN below command to generate makefiles from CMakeLists
  $ cmake ..
OUTPUT:
-- Toolchain file defaulted to '/local/home/svshuk00/STM32MPU_workspace/STM32MP15-Ecosystem-v1.0.0/Developer-Package/SDK/sysroots/x86_64-openstlinux_weston_sdk-linux/usr/share/cmake/OEToolchainConfig.cmake'
-- The C compiler identification is GNU 8.2.0
-- The CXX compiler identification is GNU 8.2.0
-- Check for working C compiler: /local/home/svshuk00/STM32MPU_workspace/STM32MP15-Ecosystem-v1.0.0/Developer-Package/SDK/sysroots/x86_64-openstlinux_weston_sdk-linux/usr/bin/arm-openstlinux_weston-linux-gnueabi/arm-openstlinux_weston-linux-gnueabi-gcc
-- Check for working C compiler: /local/home/svshuk00/STM32MPU_workspace/STM32MP15-Ecosystem-v1.0.0/Developer-Package/SDK/sysroots/x86_64-openstlinux_weston_sdk-linux/usr/bin/arm-openstlinux_weston-linux-gnueabi/arm-openstlinux_weston-linux-gnueabi-gcc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /local/home/svshuk00/STM32MPU_workspace/STM32MP15-Ecosystem-v1.0.0/Developer-Package/SDK/sysroots/x86_64-openstlinux_weston_sdk-linux/usr/bin/arm-openstlinux_weston-linux-gnueabi/arm-openstlinux_weston-linux-gnueabi-g++
-- Check for working CXX compiler: /local/home/svshuk00/STM32MPU_workspace/STM32MP15-Ecosystem-v1.0.0/Developer-Package/SDK/sysroots/x86_64-openstlinux_weston_sdk-linux/usr/bin/arm-openstlinux_weston-linux-gnueabi/arm-openstlinux_weston-linux-gnueabi-g++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /local/home/svshuk00/RFAL v2.0.4/Linux_RFAL_st25r3911_v2.0.4/linux_demo/build

4. RUN below command to build
  $ make
OUTPUT:
Scanning dependencies of target rfal_st25r3911
[  3%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_analogConfig.c.o
[  7%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_crc.c.o
[ 11%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_dpo.c.o
[ 15%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_iso15693_2.c.o
[ 19%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_isoDep.c.o
[ 23%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_nfcDep.c.o
[ 26%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_nfca.c.o
[ 30%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_nfcb.c.o
[ 34%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_nfcf.c.o
[ 38%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_nfcv.c.o
[ 42%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_st25tb.c.o
[ 46%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_t1t.c.o
[ 50%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_t2t.c.o
[ 53%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/rfal_t4t.c.o
[ 57%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/st25r3911/rfal_rfst25r3911.c.o
[ 61%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/st25r3911/st25r3911.c.o
[ 65%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/st25r3911/st25r3911_com.c.o
[ 69%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/local/home/svshuk00/RFAL_v2.0.4/Linux_RFAL_st25r3911_v2.0.4/rfal/source/st25r3911/st25r3911_interrupt.c.o
[ 73%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/__/__/platform/Src/pltf_gpio.c.o
[ 76%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/__/__/platform/Src/pltf_spi.c.o
[ 80%] Building C object rfal/st25r3911/CMakeFiles/rfal_st25r3911.dir/__/__/platform/Src/pltf_timer.c.o
[ 84%] Linking C shared library librfal_st25r3911.so
[ 84%] Built target rfal_st25r3911
Scanning dependencies of target nfc_poller_st25r3911
[ 88%] Building C object nfc_poller/CMakeFiles/nfc_poller_st25r3911.dir/Src/exampleRfalPoller.c.o
[ 92%] Building C object nfc_poller/CMakeFiles/nfc_poller_st25r3911.dir/Src/logger.c.o
[ 96%] Building C object nfc_poller/CMakeFiles/nfc_poller_st25r3911.dir/Src/main.c.o
[100%] Linking C executable nfc_poller_st25r3911
[100%] Built target nfc_poller_st25r3911

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


How to RUN the demo application on STM32MP157C-DK2 board.

1. Follow above mentioned steps to build the Package.

2. Copy below files to /usr/local folder on STM32MP157C-DK2 board.
  a. Linux_RFAL_st25r3911_v2.0.4/linux_demo/build/nfc_poller/nfc_poller_st25r3911
  b. Linux_RFAL_st25r3911_v2.0.4/linux_demo/build/rfal/st25r3911/librfal_st25r3911.so

3. On STM32MP157C-DK2 command line, export the path of shared lib -
  $ export LD_LIBRARY_PATH=/usr/local:LD_LIBRARY_PATH

5. RUN the application
 $ cd /usr/local
 $ ./nfc_poller_st25r3911

 
