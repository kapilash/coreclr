
project(System.Net.Native)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

add_compile_options(-fPIC)

set(NATIVENET_SOURCES
    corenet.cpp
)

add_library(System.Net.Native
    SHARED
    ${NATIVENET_SOURCES}
)

# Disable the "lib" prefix.
set_target_properties(System.Net.Native PROPERTIES PREFIX "")

install (TARGETS System.Net.Native DESTINATION .)
