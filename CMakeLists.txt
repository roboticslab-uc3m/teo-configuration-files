cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

# Define a project.
project(TEO_CONFIGURATION_FILES LANGUAGES NONE)

# Find dependencies.
find_package(YCM 0.11 REQUIRED)
find_package(YARP 3.7 REQUIRED)

# Set some useful variables - paths relative to the installation prefix.
yarp_configure_external_installation(teo-configuration-files)

# Standard installation directories.
include(GNUInstallDirs)

# Traverse subdirectories.
add_subdirectory(share)
add_subdirectory(scripts)

# Store the package in the user registry.
set(CMAKE_EXPORT_PACKAGE_REGISTRY ON)

# Create and install config files.
include(InstallBasicPackageFiles)

install_basic_package_files(TEO_CONFIGURATION_FILES
                            VERSION 0.1.0
                            COMPATIBILITY AnyNewerVersion
                            NO_EXPORT)

# Add uninstall rule.
include(AddUninstallTarget)
