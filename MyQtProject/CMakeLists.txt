cmake_minimum_required(VERSION 3.14)
project(MyQtProject)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Set the path to your Qt installation
set(CMAKE_PREFIX_PATH "C:/Qt/6.8.0/msvc2022_64")

# Find the required Qt packages
find_package(Qt6 COMPONENTS Widgets REQUIRED)

# Add the executable
add_executable(MyQtProject main.cpp)

# Link the Qt libraries
target_link_libraries(MyQtProject Qt6::Widgets)

# Include the Qt headers
target_include_directories(MyQtProject PRIVATE ${Qt6Widgets_INCLUDE_DIRS})