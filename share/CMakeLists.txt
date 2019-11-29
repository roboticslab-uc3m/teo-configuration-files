yarp_install(DIRECTORY applications/yarpmanager
                       applications/yarpmotorgui
                       ../doc/fig
             DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})

yarp_install(DIRECTORY contexts/kinematics
                       contexts/launchLocomotion
                       contexts/launchManipulation
             DESTINATION ${TEO-CONFIGURATION-FILES_CONTEXTS_INSTALL_DIR})
