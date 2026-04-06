# Updated CMakeLists.txt for Qt6 support
cmake_minimum_required(VERSION 3.1)
project(DuicoinCore)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

add_executable(DuicoinCore src/gui/main_window.cpp src/gui/digital_clock.cpp src/gui/world_clock.cpp)

target_link_libraries(DuicoinCore Qt6::Widgets)

# ... other configurations ...