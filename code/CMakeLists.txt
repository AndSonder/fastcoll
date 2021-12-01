project(fastcoll)
cmake_minimum_required(VERSION 2.6.2)
set(fastcoll_SOURCES
	block0.cpp
	block1.cpp
	block1stevens00.cpp
	block1stevens01.cpp
	block1stevens10.cpp
	block1stevens11.cpp
	block1wang.cpp
	main.cpp
	main.hpp
	md5.cpp)

find_package(Boost REQUIRED COMPONENTS
filesystem   
program_options
lexical_cast
timer
cstdint
)
if(NOT Boost_FOUND)
    message("Not found Boost")
endif()
 
include_directories(${Boost_INCLUDE_DIRS})
message("${Boost_INCLUDE_DIRS}")
message("${Boost_LIBRARIES}")

add_executable(fastcoll ${fastcoll_SOURCES})
target_link_libraries(fastcoll boost_system-mt boost_filesystem-mt boost_program_options-mt)
