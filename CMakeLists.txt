cmake_minimum_required(VERSION 3.2)

project(
  foo
  VERSION 0.0
  DESCRIPTION "foobar"
  LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

add_executable(foo
  src/main.cpp
  src/SDL2Wrapper/Color.cpp
  src/SDL2Wrapper/Game.cpp
  src/SDL2Wrapper/Point.cpp
  src/SDL2Wrapper/PointF.cpp
  src/SDL2Wrapper/Rect.cpp
  src/SDL2Wrapper/RectF.cpp
  src/SDL2Wrapper/Renderer.cpp
  src/SDL2Wrapper/Size.cpp
  src/SDL2Wrapper/Window.cpp
)

target_link_libraries(foo ${SDL2_LIBRARIES})
