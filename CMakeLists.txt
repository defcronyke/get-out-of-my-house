# Ⓒ Copyright 2013 Jeremy Carter
#
# This file is part of get-out-of-my-house.
#
# get-out-of-my-house is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 3, as published 
# by the Free Software Foundation.
#
# get-out-of-my-house is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with get-out-of-my-house. If not, see <http://www.gnu.org/licenses/gpl-3.0.txt>.
#
# CMakeLists.txt
#
# Created on: Oct 3, 2013
#     Author: Jeremy Carter
#      Email: Jeremy [at] JeremyCarter [dot] ca
#

project (get-out-of-my-house)
set (get-out-of-my-house_VERSION_MAJOR 0)
set (get-out-of-my-house_VERSION_MINOR 0)

cmake_minimum_required (VERSION 2.8.10)
set (CMAKE_VERBOSE_MAKEFILE ON)
set (CMAKE_BUILD_TYPE Debug)
list (APPEND CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS}")	# This project uses C++11.
file (TO_NATIVE_PATH "${PROJECT_SOURCE_DIR}/src" src_dir)	# Path to project source code.
file (TO_NATIVE_PATH "${src_dir}/cmake_modules" CMAKE_MODULE_PATH)	# Path to custom cmake modules.

add_executable (get-out-of-my-house ${src_dir}/main.cpp)
