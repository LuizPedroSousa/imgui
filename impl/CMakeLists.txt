file(GLOB_RECURSE IMGUI_IMPL_SRC
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_impl_glfw.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/imgui_impl_opengl3.cpp
)

file(GLOB_RECURSE IMGUI_IMPL_HEADERS
    ${CMAKE_CURRENT_SOURCE_DIR}/impl/imgui_impl_glfw.h
    ${CMAKE_CURRENT_SOURCE_DIR}/impl/imgui_impl_opengl3.cpp
)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/..)

add_library(imgui_impl STATIC ${IMGUI_IMPL_SRC} ${IMGUI_IMPL_HEADERS})

target_include_directories(imgui_impl PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_link_libraries(imgui_impl PRIVATE imgui)

