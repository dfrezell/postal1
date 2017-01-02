add_library(cyan STATIC
	Unix/uColors.cpp
	Unix/uDialog.cpp
	Unix/uPath.cpp)

target_link_libraries(cyan blue) 
