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

include_directories (../src ${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

add_executable (dummy_test dummy_test.cpp)
target_link_libraries (dummy_test gtest gtest_main)
add_test (dummy_test dummy_test)