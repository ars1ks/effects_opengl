cmake_minimum_required(VERSION 3.10)
project(GLFWApp)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Находим GLFW
find_package(glfw3 REQUIRED)

# Находим OpenGL
find_package(OpenGL REQUIRED)

# Создаем исполняемый файл
add_executable(glfw_app main.cpp)

# Подключаем библиотеки
target_link_libraries(glfw_app glfw ${OPENGL_LIBRARIES})
