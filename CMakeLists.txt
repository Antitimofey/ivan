cmake_minimum_required(VERSION 3.5)

set(PROJECT_NAME AI_FOR_CHECKERS)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 20)


set(SOURCES
main.cpp
saving/downloading.cpp
saving/uploading.cpp
AI/bestMoveAI.cpp
user/userMoves.cpp
window/changes.cpp
mainLoop.cpp
window/mouse.cpp
)

set(HEADERS
mainHead.hpp
AI/AI.hpp
saving/saving.hpp
user/user.hpp
window/window.hpp
)

add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})

target_include_directories(${PROJECT_NAME} PUBLIC
${CMAKE_CURRENT_SOURCE_DIR}/AI
${CMAKE_CURRENT_SOURCE_DIR}/saving
${CMAKE_CURRENT_SOURCE_DIR}/user
${CMAKE_CURRENT_SOURCE_DIR}/window
)
