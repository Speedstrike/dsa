project(tests)

add_subdirectory(lib/googletest)

include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

file(GLOB TEST_FILES *.cpp)

enable_testing()

add_executable(all_tests ${TEST_FILES} ${SRC_FILES})

target_link_libraries(all_tests PRIVATE gtest gtest_main)

set_target_properties(all_tests PROPERTIES CXX_STANDARD 20)
