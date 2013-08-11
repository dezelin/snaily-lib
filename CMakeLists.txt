#
#   This file is part of libsnaily.
#
#   Foobar is free software: you can redistribute it and/or modify
#   it under the terms of the GNU General Public License as published by
#   the Free Software Foundation, either version 3 of the License, or
#   (at your option) any later version.
#
#   Foobar is distributed in the hope that it will be useful,
#   but WITHOUT ANY WARRANTY; without even the implied warranty of
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#   GNU General Public License for more details.
#
#   You should have received a copy of the GNU General Public License
#   along with libsnaily.  If not, see <http://www.gnu.org/licenses/>.
#

cmake_minimum_required (VERSION 2.8)
project (libsnaily)


if (CMAKE_BINARY_DIR STREQUAL ${CMAKE_SOURCE_DIR})
    message(FATAL_ERROR "type: git clean -df && mkdir build && cd build && cmake .. && make")
endif()

if (CMAKE_BUILD_TYPE MATCHES Debug)
    set(CMAKE_VERBOSE_MAKEFILE 1)
else ()
    set(CMAKE_VERBOSE_MAKEFILE 0)
endif ()

add_definitions ("-Wall -std=c++11")

enable_testing ()

#add_subdirectory (3rd_party/gtest-1.6.0)
add_subdirectory (3rd_party/gmock-1.6.0)
add_subdirectory (src)
