# Copyright: UC3M 2017
# Author: roboticslab, jgvictores, etc
# CopyPolicy: Released under the terms of the GNU GPL v2.0.
# 

find_package(YARP REQUIRED)
list(APPEND CMAKE_MODULE_PATH ${YARP_MODULE_PATH})
include(YarpInstallationHelpers)
#yarp_configure_external_installation(teo-configuration-files)  # Commentig out because not using generated vars

yarp_install(PROGRAMS bash/teoSim DESTINATION ${CMAKE_INSTALL_BINDIR})

