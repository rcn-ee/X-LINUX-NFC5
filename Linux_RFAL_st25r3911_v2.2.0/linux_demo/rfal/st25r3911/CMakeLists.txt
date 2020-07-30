# Bring headers into the project
include_directories(
    ../../../rfal/include
    ../../../common/firmware/STM/utils/Inc
    ../../../rfal/source/st25r3911
    ../../../rfal/source
    ../../platform/Inc
    ../../platform/Inc/st25r3911)

# Source files to build the project
file(GLOB SOURCE1 "../../../rfal/source/*.c")
file(GLOB SOURCE2 "../../../rfal/source/st25r3911/*.c")
file(GLOB SOURCE3 "../../platform/Src/*.c")
set(SOURCE ${SOURCE1} ${SOURCE2} ${SOURCE3})

find_library(LIBRT_PATH rt)

# Create the shared library
add_library(rfal_st25r3911 SHARED ${SOURCE})

target_link_libraries(rfal_st25r3911 "${LIBRT_PATH}")
