add_library(OpenGEX
OpenGEX.cpp
)

include_directories(
${CMAKE_CURRENT_SOURCE_DIR}/../OpenDDL
)

set_target_properties(OpenGEX
PROPERTIES PUBLIC_HEADER OpenGEX.h
)

install(TARGETS OpenGEX
    ARCHIVE DESTINATION ${CMAKE_SYSTEM_NAME}/lib
    PUBLIC_HEADER DESTINATION ${CMAKE_SYSTEM_NAME}/include
)

if(${MSVC})
    install(FILES ${PROJECT_BINARY_DIR}/OpenGEX/Debug/OpenGEX.pdb
        DESTINATION ${CMAKE_SYSTEM_NAME}/lib
        CONFIGURATIONS Debug
        )
endif(${MSVC})


