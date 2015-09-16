cmake_minimum_required(VERSION 3.0.2 FATAL_ERROR)

set(CMAKE_PREFIX_PATH "D:\\QT5.5.0\\5.5\\msvc2013")

project(cmake_and_qt5)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5Widgets REQUIRED)
find_package(Qt5WebKit  REQUIRED)
find_package(Qt5WebKitWidgets REQUIRED)

add_executable(cmake_and_qt5 WIN32 main.cpp mainwindow.cpp)

qt5_use_modules(cmake_and_qt5 Widgets WebKit WebKitWidgets)

target_link_libraries(cmake_and_qt5 Qt5::Widgets Qt5::WebKit Qt5::WebKitWidgets)
