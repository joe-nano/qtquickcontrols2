# Generated from swipetoremove.pro.

cmake_minimum_required(VERSION 3.14)
project(swipetoremove LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/quickcontrols2/swipetoremove")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Qml)

add_qt_gui_executable(swipetoremove
    swipetoremove.cpp
)
target_link_libraries(swipetoremove PUBLIC
    Qt::Core
    Qt::Gui
    Qt::Qml
)


# Resources:
set(qmake_immediate_resource_files
    "fonts/fontello.ttf"
    "swipetoremove.qml"
)

qt6_add_resources(swipetoremove "qmake_immediate"
    PREFIX
        "/"
    FILES
        ${qmake_immediate_resource_files}
)

install(TARGETS swipetoremove
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
