include_directories(include/)
add_executable(BasicRect src/BasicRect.cpp src/glad.c)
add_executable(GLTest src/GLTest.cpp src/glad.c)

find_library(CARBON_LIBRARY Carbon)
find_library(COCOA_LIBRARY Cocoa)
find_library(IOKIT_LIBRARY IOKit)

target_link_libraries(BasicRect glfw3 ${CARBON_LIBRARY} ${COCOA_LIBRARY} ${IOKIT_LIBRARY})
target_link_libraries(GLTest glfw3 ${CARBON_LIBRARY} ${COCOA_LIBRARY} ${IOKIT_LIBRARY})
