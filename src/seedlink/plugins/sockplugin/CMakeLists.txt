SET(SOCKPLUGIN_SOURCES
	seedutils.c
	sock_plugin.c
	../plugin.c
)

INCLUDE_DIRECTORIES(.)
INCLUDE_DIRECTORIES(..)

ADD_EXECUTABLE(sock_plugin ${SOCKPLUGIN_SOURCES})
TARGET_LINK_LIBRARIES(sock_plugin m)

INSTALL(TARGETS sock_plugin RUNTIME DESTINATION ${SEEDLINK_PLUGIN_OUTPUT_DIR})
