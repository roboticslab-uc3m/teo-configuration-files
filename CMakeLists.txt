# Copyright: Universidad Carlos III de Madrid (C) 2017;
# Authors: Juan G. Victores & Raul de Santos Rico
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

cmake_minimum_required(VERSION 2.8.9)

project(TEO_CONFIGURATION_FILES)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake)

add_subdirectory(share)
add_subdirectory(scripts)

include(GNUInstallDirs)

if(WIN32 AND NOT CYGWIN)
    set(_cmake_destination CMake)
else()
    set(_cmake_destination ${CMAKE_INSTALL_LIBDIR}/cmake/TEO_CONFIGURATION_FILES)
endif()

export(PACKAGE TEO_CONFIGURATION_FILES)

file(WRITE ${CMAKE_BINARY_DIR}/TEO_CONFIGURATION_FILESConfig.cmake "# Dummy CMake configuration export file.")
install(FILES ${CMAKE_BINARY_DIR}/TEO_CONFIGURATION_FILESConfig.cmake DESTINATION ${_cmake_destination})

# uninstall target
configure_file(
    "${CMAKE_CURRENT_SOURCE_DIR}/cmake/template/TEO_CONFIGURATION_FILESConfigUninstall.cmake.in"
    "${CMAKE_CURRENT_BINARY_DIR}/TEO_CONFIGURATION_FILESConfigUninstall.cmake" IMMEDIATE @ONLY)

add_custom_target(uninstall
    COMMAND ${CMAKE_COMMAND} -P ${CMAKE_CURRENT_BINARY_DIR}/TEO_CONFIGURATION_FILESConfigUninstall.cmake)
