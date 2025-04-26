include(AddCatch2)

add_executable(unit_tests
    Test_AudioIO.cpp 
    # Test_BeatHisto.cpp 
    # Test_Chords.cpp 
    # Test_Dtw.cpp 
    # Test_Features.cpp 
    # Test_Fft.cpp 
    # Test_Filter.cpp 
    # Test_Key.cpp 
    # Test_Matrix.cpp 
    # Test_Novelty.cpp 
    # Test_Pitch.cpp 
    # Test_RingBuffer.cpp 
    # Test_Spectrogram.cpp 
    # Test_Tools.cpp
)

target_link_libraries(
  unit_tests PRIVATE libACA Catch2::Catch2
)

target_include_directories(unit_tests PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})

include(CTest)
include(Catch)
catch_discover_tests(unit_tests)