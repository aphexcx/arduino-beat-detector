cmake_minimum_required(VERSION 3.7)
set(CMAKE_TOOLCHAIN_FILE ${CMAKE_SOURCE_DIR}/cmake/ArduinoToolchain.cmake)
set(PROJECT_NAME Sound_Sampler)
project(${PROJECT_NAME})

set(${CMAKE_PROJECT_NAME}_SKETCH BeatDetector/beat_detector.ino)

#### Uncomment below additional settings as needed.
set(${CMAKE_PROJECT_NAME}_BOARD nano)
set(${CMAKE_PROJECT_NAME}_PORT /dev/cu.wchusbserial1420)
set(nano.build.mcu atmega328p)
set(nano.upload.speed 57600)
# set(mega.build.mcu atmega328)
# set(mega.upload.protocol wiring)
# set(mega.upload.speed 115200)

generate_arduino_firmware(${CMAKE_PROJECT_NAME})
