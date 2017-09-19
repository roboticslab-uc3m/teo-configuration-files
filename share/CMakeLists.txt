# Copyright: UC3M 2017
# Author: roboticslab, jgvictores, etc
# CopyPolicy: Released under the terms of the GNU GPL v2.0.
# 

find_package(YARP REQUIRED)
list(APPEND CMAKE_MODULE_PATH ${YARP_MODULE_PATH})
include(YarpInstallationHelpers)
yarp_configure_external_installation(teo-configuration-files)

yarp_install(FILES ymanager.ini DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})
yarp_install(FILES yarpmotorgui/teo-yarpmotorgui.ini DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})
yarp_install(FILES yarpmotorgui/teoSim-yarpmotorgui.ini DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})
yarp_install(FILES ../doc/fig/teo-apps-64x64.png DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})

### Go through single applications

add_subdirectory(kinematics)
add_subdirectory(teoBase)
add_subdirectory(teoSimBase)
add_subdirectory(teoTools)
add_subdirectory(yarpmotorgui)

