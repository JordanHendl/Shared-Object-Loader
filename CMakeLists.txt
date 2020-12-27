set( KARMA_SOL_SOURCES 
     ObjectLoader.cpp
   )

set( KARMA_SOL_HEADERS
     ObjectLoader.h
   )

add_library( karma_sol SHARED ${KARMA_SOL_SOURCES} ${KARMA_SOL_HEADERS} )
