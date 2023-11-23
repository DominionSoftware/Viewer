cmake_minimum_required(VERSION 3.20.0)
project(${PROJECT_NAME})




message(STATUS "Qt6_DIR")
message(${Qt6_DIR})

 



set(SOURCE
	main.cpp
)

set(HEADERS_MOC_HPP

)

set(VIEWER_RESOURCES

)
add_executable(${PROJECT_NAME} 
	${SOURCE}
	${HEADERS_MOC_HPP}
	 
	${RESOURCES}
)

#target_include_directories(${PROJECT_NAME} ${Qt6Widgets_INCLUDE_DIRS})

target_link_libraries(${PROJECT_NAME}  Qt6::Widgets)


 
  message(STATUS "print_all_variables------------------------------------------{")
  get_cmake_property(_variableNames VARIABLES)
  foreach (_variableName ${_variableNames})
      message(STATUS "${_variableName}=${${_variableName}}")
  endforeach()
  message(STATUS "print_all_variables------------------------------------------}")
 
