add_library(OpenDDL
ODDLMap.cpp
ODDLString.cpp
ODDLTree.cpp
OpenDDL.cpp
)

set(HEADER_FILES OpenDDL.h ODDLArray.h
    ODDLMap.h
    ODDLString.h
    ODDLTree.h
    ODDLTypes.h
    )

set_target_properties(OpenDDL
    PROPERTIES PUBLIC_HEADER "${HEADER_FILES}"
)

install(TARGETS OpenDDL
    ARCHIVE DESTINATION lib
    PUBLIC_HEADER DESTINATION include
)

