include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../..)

set(generator_smoke_SRC
    generator_smoke.cpp
    writeClasses.cpp
    writeSmokeDataFile.cpp
    helpers.cpp)

add_library(generator_smoke MODULE ${generator_smoke_SRC})
target_link_libraries(generator_smoke ${QT_QTCORE_LIBRARY} ${QT_QTXML_LIBRARY} smokegen)
set_target_properties(generator_smoke PROPERTIES PREFIX "")

install(TARGETS generator_smoke LIBRARY DESTINATION ${LIB_INSTALL_DIR}/smokegen/)
