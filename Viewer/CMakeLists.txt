cmake_minimum_required(VERSION 3.20.0)


set(ROOT_PROJECT_NAME Viewer)

project(${ROOT_PROJECT_NAME})

#if WIN32()
set(CMAKE_CXX_FLAGS
	"${CMAKE_CXX_FLAGS} /MP /EHsc /W3 /we4238 /we4350 /we4239"
)
#else()

#endif()


get_filename_component(PARENT_DIR ${CMAKE_CURRENT_SOURCE_DIR} DIRECTORY)

set(LIBSLOCATION "${PARENT_DIR}")

message(STATUS "${LIBSLOCATION}")
set(Qt6_LOCATION "${LIBSLOCATION}/qt6.ins/lib/cmake/Qt6/")
message(STATUS "${Qt6_LOCATION}")



set(Qt6_DIR ${Qt6_LOCATION} CACHE PATH "Qt6 Dir")
message(STATUS "${Qt6_DIR}")

message(STATUS "${Qt6_DIR}=${${Qt6_DIR}}")
find_package(Qt6 REQUIRED)


set(PROJECT_NAME ${ROOT_PROJECT_NAME}.Viewer)


add_subdirectory(Source)

# dump all variables for debugging.
get_cmake_property(_variableNames VARIABLES)
foreach (_variableName ${_variableNames})
    message(STATUS "${_variableName}=${${_variableName}}")
endforeach()