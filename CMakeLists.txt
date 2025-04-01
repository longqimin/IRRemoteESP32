# CMakeFiles.txt inside "IRemoteESP8266" folder
cmake_minimum_required(VERSION 3.5)

set(srcs
    src/IRRemoteESP32.cpp
)

set(includedirs
    include
)

set(srcs ${srcs})

idf_component_register(INCLUDE_DIRS ${includedirs} SRCS ${srcs} REQUIRES "arduino-esp32")

target_compile_definitions(${COMPONENT_LIB} PRIVATE -D ESP32 -D ARDUINO)
message(STATUS "COMPONENT_LIB = ${COMPONENT_LIB}")

# idf_component_register(SRCS
# INCLUDE_DIRS "src/."
# REQUIRES "arduino" # Library requires Arduino
# )
project(IRemoteESP8266)