cmake_minimum_required(VERSION 3.4.1)
# using unicode in VS
if(MSVC)
    ADD_DEFINITIONS(-DUNICODE)
    ADD_DEFINITIONS(-D_UNICODE)
endif(MSVC)

set(API
    imconfig.h
    imgui.h
    imgui_internal.h
    stb_rect_pack.h
    stb_textedit.h
    stb_truetype.h
)

set(SRC
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
)

add_library(imgui STATIC ${API} ${SRC})
