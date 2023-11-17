cmake_minimum_required(VERSION 3.20.0)
project(${PROJECT_NAME})

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

 
