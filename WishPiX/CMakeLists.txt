add_library(wishpix STATIC
	Menu/menu.cpp
	Menu/menu.h
	Prefs/prefline.cpp
	Prefs/prefline.h
	Prefs/prefs.cpp
	Prefs/prefs.h
	ResourceManager/resmgr.cpp
	ResourceManager/resmgr.h
	Spry/spry.cpp
	Spry/spry.h)

target_include_directories(wishpix PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}
	${PROJECT_SOURCE_DIR}
	${PROJECT_SOURCE_DIR}/RSPiX/Inc)

target_link_libraries(wishpix blue)
