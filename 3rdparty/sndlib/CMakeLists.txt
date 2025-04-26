add_library(sndlib
    audio.c 
    clm.c 
    clm2xen.c 
    headers.c 
    io.c 
    s7.c 
    sndinfo.c 
    sndlib2xen.c 
    sndplay.c 
    sound.c 
    vct.c 
    xen.c
)

target_include_directories(sndlib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})