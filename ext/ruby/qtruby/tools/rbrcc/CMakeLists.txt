SET(rbrcc_SRCS rcc.cpp main.cpp )

ADD_EXECUTABLE(rbrcc ${rbrcc_SRCS})
TARGET_LINK_LIBRARIES (rbrcc ${QT_QTCORE_LIBRARY} ${QT_QTXML_LIBRARY})

INSTALL(TARGETS rbrcc DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)
