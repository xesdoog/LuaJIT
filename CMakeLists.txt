cmake_minimum_required(VERSION 3.0...4.0)

list(APPEND CMAKE_MODULE_PATH
  "${CMAKE_CURRENT_SOURCE_DIR}/cmake"
  "${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules"
)

set(LUAJIT_TOP_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

project(luajit)

set(can_use_assembler TRUE)

if (MSVC)
    enable_language(ASM_MASM)
else()
    enable_language(ASM)
endif()

include (GNUInstallDirs)

add_subdirectory(src)
