# CMakeList.txt : CMake project for cpp-bad_apple, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.12)

project ("cpp-bad_apple")

# Add source to this project's executable.
add_executable (cpp-bad_apple "cpp-bad_apple.cpp" "cpp-bad_apple.h")

find_package(SFML COMPONENTS system window graphics audio CONFIG REQUIRED)
target_link_libraries(cpp-bad_apple PRIVATE sfml-system sfml-network sfml-graphics sfml-window sfml-audio)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET cpp-bad_apple PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
