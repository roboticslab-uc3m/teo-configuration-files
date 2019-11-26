# Copyright: UC3M 2019
# Author: roboticslab, jgvictores, etc
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

yarp_install(DIRECTORY applications/yarpmanager
                       applications/yarpmotorgui
                       ../doc/fig
             DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})

yarp_install(DIRECTORY contexts/kinematics
                       contexts/launchCanBus
             DESTINATION ${TEO-CONFIGURATION-FILES_CONTEXTS_INSTALL_DIR})

yarp_install(DIRECTORY robots/teo
             DESTINATION ${TEO-CONFIGURATION-FILES_ROBOTS_INSTALL_DIR})
