add_library(rvfft
    rvfft.cpp
)

if (MSVC)
    target_compile_options(rvfft PUBLIC -D_USE_MATH_DEFINES)
endif()

target_include_directories(rvfft PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})