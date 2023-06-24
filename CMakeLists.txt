file(GLOB_RECURSE IMGUI_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_internal.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_tables.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_widgets.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_draw.cpp
)
file(GLOB_RECURSE IMGUI_HEADERS
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui.h
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_internal.h
)


add_library(imgui STATIC ${IMGUI_SRC} ${IMGUI_HEADERS})


include_directories(${CMAKE_CURRENT_SOURCE_DIR})

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
