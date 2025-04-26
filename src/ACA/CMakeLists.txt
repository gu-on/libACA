add_library(libACA
    AcaAll.cpp
    BeatHisto.cpp
    Chord.cpp
    ChordFromBlock.cpp
    Feature.cpp
    FeatureFromBlock.cpp
    Fft.cpp
    Key.cpp
    KeyFromChroma.cpp
    Novelty.cpp
    NoveltyFromBlock.cpp
    Pitch.cpp
    PitchFromBlock.cpp
    Spectrogram.cpp
    SubFingerprint.cpp
    ToolBlockAudio.cpp
    ToolCcf.cpp
    ToolConversion.cpp
    ToolFingerprint.cpp
    ToolGammatone.cpp
    ToolGmm.cpp
    ToolGmmClassifier.cpp
    ToolLeaveOneOutCrossVal.cpp
    ToolNmf.cpp
    ToolPca.cpp
    ToolSeqFeatureSel.cpp
    ToolSimpleDtw.cpp
    ToolSimpleKmeans.cpp
    ToolSimpleKnn.cpp
    ToolViterbi.cpp
)

target_link_libraries(libACA PUBLIC rvfft)
target_include_directories(libACA PUBLIC ${ACA_SOURCE_DIR}/inc ${ACA_SOURCE_DIR}/inc/helper ${CMAKE_BINARY_DIR}/inc)