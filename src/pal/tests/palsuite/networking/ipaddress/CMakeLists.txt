cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  localhostaddrs.c
)

add_executable(paltest_getaddrs_test1
  ${SOURCES}
)

add_dependencies(paltest_getaddrs_test1 System.Net.Native)

target_link_libraries(paltest_getaddrs_test1
  pthread
  m
  System.Net.Native
)
