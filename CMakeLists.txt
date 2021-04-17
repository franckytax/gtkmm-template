cmake_minimum_required(VERSION 3.0.0)

project(Fenetre)

find_package(PkgConfig)
pkg_check_modules(GTKMM gtkmm-3.0)

if(NOT GTKMM_FOUND)
    message(FATAL_ERROR "gtkmm-3.0 not found!")
endif()

link_directories(
    ${GTKMM_LIBRARY_DIRS}
)
include_directories(
    ${GTKMM_INCLUDE_DIRS}
)

set(SRC src/main.cpp src/Fenetre.cpp)

add_executable(
    Fenetre
    ${SRC}
)

target_link_libraries(
    Fenetre
    ${GTKMM_LIBRARIES}
)