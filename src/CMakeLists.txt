cmake_minimum_required(VERSION 2.8.12)

file(GLOB SOURCE_FILES *.cpp *.h)

set(LIBS rzu)
if(WIN32)
    list(APPEND LIBS Winmm.lib)
endif()

add_exe(${TARGET_NAME} "${SOURCE_FILES}" "${LIBS}")
