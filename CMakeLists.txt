cmake_minimum_required(VERSION 3.9)
project (tiles-with-data)

add_subdirectory(vendor/osmpbf osmpbf)

set(SOURCES_CPP
	src/main.cpp
)

add_executable(${PROJECT_NAME} ${SOURCES_CPP})
target_link_libraries(${PROJECT_NAME} PUBLIC osmpbf)
target_compile_features(${PROJECT_NAME} PUBLIC cxx_std_17)

