add_library(Wire Wire/Wire.cpp Wire/Wire.h)
add_library(libs::Wire ALIAS Wire)
target_include_directories(Wire
        PUBLIC
        $<INSTALL_INTERFACE:include>
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/Wire>
)
target_link_libraries(Wire PRIVATE cores::esp8266)