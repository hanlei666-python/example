cmake_minimum_required(VERSION 3.0.0)
project(main.c VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(main.c main.c)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Widgets)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Widgets)

include_directories(D:/ffmpeg/include)
include_directories(D:/OpenSSL-Win32/include)
link_directories(D:/ffmpeg/lib)
link_directories(D:/OpenSSL-Win32/lib)
