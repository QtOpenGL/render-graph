cmake_minimum_required(VERSION 3.1)

add_library(RenderGraph RenderGraph.h Factory.cpp Factory.h Instance.cpp Instance.h Pass.cpp Pass.h Framebuffer.cpp Framebuffer.h Operation.cpp Operation.h Texture.cpp Texture.h Formats.cpp Formats.h VM.h)

target_link_libraries(RenderGraph PUBLIC Graph)
target_link_libraries(RenderGraph PUBLIC OpenGL::GL)
target_include_directories(RenderGraph INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}")
