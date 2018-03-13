# Copyright: UC3M 2017
# Author: roboticslab, jgvictores, etc
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

include(GNUInstallDirs)

yarp_install(PROGRAMS bash/teoSim DESTINATION ${CMAKE_INSTALL_BINDIR})
