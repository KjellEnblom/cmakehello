# Almost all CMake files should start with this
# You should always specify a range with the newest
# and oldest tested versions of CMake. This will ensure
# you pick up the best policies.
cmake_minimum_required(VERSION 3.16)

# This is your project statement. You should always list languages;
# Listing the version is nice here since it sets lots of useful variables
project(
  cmakehello
  VERSION 1.2
  LANGUAGES C)

# If you set any CMAKE_ variables, that can go here.
# (But usually don't do this, except maybe for C++ standard)
set(CMAKE_INSTALL_PREFIX "/opt/cmakehello")

# Find packages go here.

# You should usually split this into folders, but this is a simple example

# Link each target with other targets or add options, etc.

# Adding something we can run - Output name matches target name
add_executable(cmakehello cmakehello.c)
install(TARGETS ${PROJECT_NAME} DESTINATION bin)
