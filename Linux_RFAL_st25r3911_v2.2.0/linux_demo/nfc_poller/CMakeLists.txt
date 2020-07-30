# Bring headers into the project
include_directories(
    ../../common/firmware/STM/utils/Inc
    ../platform/Inc
    ../platform/Inc/${RFAL_VARIANT}
    ../../rfal/include
    ../../rfal/source/${RFAL_VARIANT}
    ./Inc)

file(GLOB SOURCES "Src/*.c")


# Directory in which the linker will look for the library (must be set before the add_executable() command!)
link_directories(../build/rfal/${RFAL_VARIANT})


# Set the executable name
add_executable(nfc_poller_${RFAL_VARIANT} ${SOURCES})


set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
#target_link_libraries(nfc_poller_${RFAL_VARIANT} PRIVATE Threads::Threads)

# Set the library to link with
target_link_libraries(nfc_poller_${RFAL_VARIANT} PRIVATE Threads::Threads librfal_${RFAL_VARIANT}.so)
#target_link_libraries(nfc_poller_${RFAL_VARIANT} librfal_${RFAL_VARIANT}.so)
