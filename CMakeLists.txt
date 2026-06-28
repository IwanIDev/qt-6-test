cmake_minimum_required(VERSION 3.16)
project(TestQt6App VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets)

set(PROJECT_SOURCES
  src/main.cpp
  src/mainwindow.cpp
  include/mainwindow.h
)

add_executable(TestQt6App
  ${PROJECT_SOURCES}
)

target_include_directories(TestQt6App PRIVATE include)

target_link_libraries(TestQt6App PRIVATE Qt6::Core Qt6::Gui Qt6::Widgets)
