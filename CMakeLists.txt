cmake_minimum_required(VERSION 3.6)
project( DisplayImage )
set(CMAKE_CXX_STANDARD 17)                                                          # set C++ version 17

EXECUTE_PROCESS( COMMAND uname -m COMMAND tr -d '\n' OUTPUT_VARIABLE ARCHITECTURE ) # find computer architecture
message( STATUS "Architecture: ${ARCHITECTURE}" )                                   # print architecture
# if (${ARCHITECTURE} STREQUAL "arm64")
#     set(CMAKE_SYSTEM_PROCESSOR arm)
# else ()
#     message( FATAL_ERROR "incompatible architecture" )
# endif ()

find_package( OpenCV REQUIRED )
include_directories( /opt/homebrew/Cellar/opencv/4.10.0_3/include/opencv4 )

add_executable( DisplayImage DisplayImage.cpp )

file(GLOB libraries
     "/opt/homebrew/Cellar/opencv/4.10.0_3/lib/*.dylib"
     "/opt/homebrew/Cellar/opencv/4.10.0_3/lib/*.a"
)

target_link_libraries( DisplayImage ${libraries} )