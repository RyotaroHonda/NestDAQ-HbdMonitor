set(MY_TARGET mydecoder)
set(MY_PUB_HEADER
    "NodeHeaderSchema.hh"
    "NodeHeaderDecoder.hh"
    "LeafSchema.hh"
    "LeafDecoder.hh"
    "LeafProcessor.hh"
  )

file(GLOB_RECURSE SRCS "*.cc")

add_library(${MY_TARGET} STATIC
  ${SRCS}
  )

target_include_directories(${MY_TARGET} PRIVATE
  ${CMAKE_CURRENT_SOURCE_DIR}
   )

set_target_properties(${MY_TARGET} PROPERTIES
  PUBLIC_HEADER "${MY_PUB_HEADER}"
  )

install(TARGETS ${MY_TARGET}
  ARCHIVE       DESTINATION ${CMAKE_INSTALL_LIBDIR}
  PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
  )

