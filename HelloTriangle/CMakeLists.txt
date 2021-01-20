cmake_minimum_required(VERSION 3.0)

project(HelloTriangle)

include_directories(/usr/local/include)
include_directories(${PROJECT_SOURCE_DIR}/../ThirdParty/include)

link_directories(${PROJECT_SOURCE_DIR}/../ThirdParty/lib)
link_directories(/usr/local/lib)

add_executable(HelloTriangle main.cpp ${PROJECT_SOURCE_DIR}/../ThirdParty/src/glad.c)
target_link_libraries(HelloTriangle glfw3 GL X11 pthread dl)