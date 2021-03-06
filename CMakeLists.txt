# Generated by "yarp cmake"

# A cmake file to get started with for new YARP projects.
# It assumes you want to build an executable from source code in 
# the current directory.

cmake_minimum_required(VERSION 2.8.9)
set(PROJECTNAME yarpviz)
project(${PROJECTNAME})


set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Find YARP.  Point the YARP_DIR environment variable at your build.
find_package(YARP REQUIRED)

# Find YARP.  Point the YARP_DIR environment variable at your build.
find_package(YARP REQUIRED)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules)
list(APPEND CMAKE_MODULE_PATH ${YARP_MODULE_PATH})

# include some helper functions
include(GNUInstallDirs)
include(YarpInstallationHelpers)
#include(YarpUseQt5)


# setting default compilation to release/optmized
if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the type of build, recommanded options are: Debug or Release" FORCE)
endif()

# enable RPATH
option(ENABLE_RPATH "Enable RPATH for this library" ON)
mark_as_advanced(ENABLE_RPATH)
include(AddInstallRPATHSupport)
add_install_rpath_support(BIN_DIRS "${CMAKE_INSTALL_PREFIX}/${CMAKE_INSTALL_BINDIR}"
                          LIB_DIRS "${CMAKE_INSTALL_PREFIX}/${CMAKE_INSTALL_LIBDIR}"
                          DEPENDS ENABLE_RPATH
                          USE_LINK_PATH)

find_package(Graphviz)
find_package(Qt5Widgets)
#find_package(Qt5Declarative)


add_subdirectory(QGVCore)
add_subdirectory(src)
add_subdirectory(app)

