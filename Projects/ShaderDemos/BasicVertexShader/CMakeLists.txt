# CMakeList.txt : CMake project for BasicVertexShader, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

# Enable Hot Reload for MSVC compilers if supported.
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

project ("BasicVertexShader")

# Add source to this project's executable.
add_executable (BasicVertexShader   "src/main.cpp" "src/main.h")

# Add include directories for GLFW
target_include_directories(BasicVertexShader PRIVATE 
    "D:/development/libraries/GLFW/include"
)

# Add library directories for GLFW
target_link_directories(BasicVertexShader PRIVATE 
    "D:/development/libraries/GLFW/lib"
)

target_link_libraries(BasicVertexShader PRIVATE glfw3)

target_include_directories(BasicVertexShader PRIVATE 
    "D:/development/libraries/GLM"
)

find_package(OpenGL REQUIRED)

target_link_libraries(BasicVertexShader PRIVATE OpenGL::GL)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET BasicVertexShader PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
