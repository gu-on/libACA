add_library(libFileIO
    AudioFile.cpp
    AudioFileIf.cpp
)

target_link_libraries(libFileIO PUBLIC sndlib)
target_include_directories(libFileIO PUBLIC ${ACA_SOURCE_DIR}/inc ${ACA_SOURCE_DIR}/inc/helper)