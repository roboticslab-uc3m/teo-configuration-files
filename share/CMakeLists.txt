yarp_install(FILES applications/ymanager.ini
                   applications/teoBase.xml
                   applications/teoSimBase.xml
                   applications/teoSimTools.xml
                   applications/teoTools.xml
             DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})

yarp_install(DIRECTORY yarpmotorgui
                       ../doc/fig
             DESTINATION ${TEO-CONFIGURATION-FILES_DATA_INSTALL_DIR})

yarp_install(DIRECTORY contexts/kinematics
                       contexts/launchCanBus
             DESTINATION ${TEO-CONFIGURATION-FILES_CONTEXTS_INSTALL_DIR})

yarp_install(DIRECTORY robots/teo
             DESTINATION ${TEO-CONFIGURATION-FILES_ROBOTS_INSTALL_DIR})
