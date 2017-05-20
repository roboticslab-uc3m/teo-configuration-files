# Copyright: 2014 UC3M
# Author: Juan G Victores
# CopyPolicy: Released under the terms of the GNU GPL v2.0.

set(appname teoTools)

#file(GLOB conf ${CMAKE_CURRENT_SOURCE_DIR}/conf/*.ini)
#file(GLOB templates ${CMAKE_CURRENT_SOURCE_DIR}/scripts/*.template)
file(GLOB scripts ${CMAKE_CURRENT_SOURCE_DIR}/scripts/*.xml)

#yarp_install(FILES ${conf} DESTINATION ${TEO-CONFIGURATION-FILES_CONTEXTS_INSTALL_DIR}/${appname})
#yarp_install(FILES ${templates} DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_TEMPLATES_INSTALL_DIR})
yarp_install(FILES ${scripts} DESTINATION ${TEO-CONFIGURATION-FILES_APPLICATIONS_INSTALL_DIR})

