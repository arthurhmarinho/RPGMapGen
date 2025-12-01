cmake_minimum_required(VERSION 3.20)
project(RPGMapGenerator)

set(CMAKE_CXX_STANDARD 20)

# Adicionar dependências
add_subdirectory(vendor/raylib)
# (Adicione imgui e outros aqui)

# Seus arquivos
file(GLOB_RECURSE SOURCES "src/*.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})

# Linkar bibliotecas
target_link_libraries(${PROJECT_NAME} raylib raylib_imgui)
# Incluir diretórios de header
target_include_directories(${PROJECT_NAME} PRIVATE src vendor)
