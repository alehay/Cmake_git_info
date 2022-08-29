cmake_minimum_required(VERSION 3.2)
project(hello-world)

set(VERSION_TRACKING_MODULE_PATH "" CACHE STRING "The location of the cmake-git-version-tracking repository")

add_subdirectory(git_version_tracking)
include_directories(git_version_tracking)


# Setup a demo executable that links to the git library.
add_executable(demo main.cc)
target_link_libraries(demo git_info)
