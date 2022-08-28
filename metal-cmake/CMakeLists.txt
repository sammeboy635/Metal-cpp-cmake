# Library definition
cmake_minimum_required(VERSION 3.23)
set(CMAKE_CXX_STANDARD 17)
set(SOURCE_FILES main.cpp)

project(metal)


# Add main.cpp file of project root directory as source file


add_executable(main ${SOURCE_FILES})

target_include_directories(main PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}/include/metal-cpp"
        "${CMAKE_CURRENT_SOURCE_DIR}/include/metal-cpp-extensions"
        )

target_link_libraries(main PRIVATE
        "-framework Metal"
        "-framework MetalKit"
        "-framework AppKit"
        "-framework Foundation"
        "-framework QuartzCore"
        )
