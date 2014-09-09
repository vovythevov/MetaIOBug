cmake_minimum_required(VERSION 2.8.7)

project(MetaIOBug)

find_package(VTK)
include(${VTK_USE_FILE})

find_package(ITK)
include(${ITK_USE_FILE})

set(KIT_SRCS
  )

set(KIT_MOC_SRCS
  )

set(KIT_RESOURCES
  )

include_directories(
  BEFORE
  ${VTK_INCLUDE_DIRS}
  )
include_directories(
  AFTER
  ${ITK_INCLUDE_DIRS}
  ${CMAKE_CURRENT_SOURCE_DIR}
  ${CMAKE_CURRENT_BINARY_DIR}
  )
add_executable(MetaIOBug main.cpp ${KIT_SRCS})
target_link_libraries(MetaIOBug ${ITK_LIBRARIES} ${VTK_LIBRARIES})
