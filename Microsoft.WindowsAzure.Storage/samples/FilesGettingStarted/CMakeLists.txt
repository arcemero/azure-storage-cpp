include_directories(. ${AZURESTORAGESAMPLES_INCLUDE_DIRS})

# THE ORDER OF FILES IS VERY /VERY/ IMPORTANT
if(UNIX)
  set(SOURCES
     Application.cpp
     stdafx.cpp
    )
endif()

buildsample(${AZURESTORAGESAMPLES_FILES} ${SOURCES})

# Copy test configuration to output directory
file(COPY DataFile.txt DESTINATION ${CMAKE_RUNTIME_OUTPUT_DIRECTORY})
