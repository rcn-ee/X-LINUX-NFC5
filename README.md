# X-LINUX-NFC5
Linux Based application for evaluating ST25R3911B high performance NFC front-ends. ( Platform :: OpenSTLinux + STM32MP157C-DK2)

Author: Subodh Vikram SHUKLA

How to build :

Download and install the SDK for cross-compilation of the package. Please follow below link - https://wiki.st.com/stm32mpu/wiki/Getting_started/STM32MP1_boards/STM32MP157x-DK2/Develop_on_Arm%C2%AE_Cortex%C2%AE-A7/Install_the_SDK

Set environment using the ST SDK script. Find SDK and more details @ above link 

Enter the build directory in the Demo application source code 
 $ cd Linux_RFAL_st25r3911_v2.2.0/linux_demo/build

RUN below command to generate makefiles from CMakeLists 
 $ cmake ..

RUN below command to build the package 
 $ make

Below two files will be genrated :

a. Executable binary: RFAL_STMPU_release_v1.0/NFCPollerApplication/Source/Linux_RFAL_st25r3911_v2.2.0/linux_demo/build/nfc_poller/nfc_poller_st25r3911 b. Shared library: RFAL_STMPU_release_v1.0/NFCPollerApplication/Source/Linux_RFAL_st25r3911_v2.2.0/linux_demo/build/rfal/st25r3911/librfal_st25r3911.so

Copy above two files to '/usr/local' location on STM32MP157C-DK2 and run below commands to run the application -

 $ cd /usr/local 
 $ export LD_LIBRARY_PATH=/usr/local/:$LD_LIBRARY_PATH 
 $ ./nfc_poller_st25r3911
