add_library(hagl_hal INTERFACE)

target_sources(hagl_hal INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/hagl_hal.c
)

find_package(SDL2 REQUIRED)

target_include_directories(hagl_hal INTERFACE 
    ${SDL2_INCLUDE_DIRS} ${CMAKE_CURRENT_LIST_DIR}/include
)

target_link_libraries(hagl_hal INTERFACE ${SDL2_LIBRARIES})
