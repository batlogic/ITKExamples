cmake_minimum_required(VERSION 3.10.2)

project( FilterAndParallelizeImageRegion )

find_package( ITK 5.0 REQUIRED )
include( ${ITK_USE_FILE} )

add_executable( FilterAndParallelizeImageRegion Code.cxx )
target_link_libraries( FilterAndParallelizeImageRegion ${ITK_LIBRARIES} )

install( TARGETS FilterAndParallelizeImageRegion
  DESTINATION bin/ITKExamples/Core/Common
  COMPONENT Runtime
)

install( FILES Code.cxx CMakeLists.txt
  DESTINATION share/ITKExamples/Code/Core/Common/FilterAndParallelizeImageRegion
  COMPONENT Code
)

enable_testing()
add_test( NAME FilterAndParallelizeImageRegionTest
  COMMAND ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/FilterAndParallelizeImageRegion )
