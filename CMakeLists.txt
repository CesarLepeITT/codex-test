cmake_minimum_required(VERSION 3.13)
project(pico_w_keypad_led C CXX)

# Documentation-oriented placeholder CMake file.
# The firmware source uses Arduino APIs and is typically built with Arduino IDE/PlatformIO.

add_custom_target(info ALL
  COMMAND ${CMAKE_COMMAND} -E echo "Use Arduino IDE or PlatformIO to build src/main.cpp for Pico W."
)
