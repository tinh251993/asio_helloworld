cmake_minimum_required(VERSION 3.12)


set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++11")

project(asio)

message(STATUS ${CMAKE_CURRENT_SOURCE_DIR})
message(status ${CMAKE_CURRENT_SOURCE_DIR})

add_executable(
	asio
	../src/main.cpp
)


target_include_directories(asio 
				PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
				)


target_link_libraries(asio ws2_32 wsock32 ${CMAKE_CURRENT_SOURCE_DIR}../include )