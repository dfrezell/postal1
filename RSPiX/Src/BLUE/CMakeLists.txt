add_library(blue STATIC
	unix/Bdebug.cpp
	unix/Bdisp.cpp
	unix/Bjoy.cpp
	unix/Bkey.cpp
	unix/Bmain.cpp
	unix/Bmouse.cpp
	unix/Bsound.cpp
	unix/Btime.cpp)

target_include_directories(blue PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}
	${CMAKE_CURRENT_SOURCE_DIR}/..
	${PROJECT_SOURCE_DIR}/SDL2/include)

target_compile_options(blue PUBLIC -fsigned-char)
target_compile_options(blue PUBLIC -w -g)
