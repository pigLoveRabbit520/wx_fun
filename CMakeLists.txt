cmake_minimum_required(VERSION 3.2)

project(wx_fun)

set(SOURCE src/main.cpp)

set(wxWidgets_ROOT_DIR $ENV{WXWIN})
set(wxWidgets_LIB_DIR $ENV{WXWIN}/lib/gcc_lib)
set(wxWidgets_CONFIGURATION mswu)

add_executable(${PROJECT_NAME} WIN32 ${SOURCE})
find_package(wxWidgets COMPONENTS net core base)
if(wxWidgets_FOUND)
  include(${wxWidgets_USE_FILE})
  target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
endif()