cmake_minimum_required(VERSION 4.0)
project(c_learn)

aux_source_directory(src SOURCES)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/main.c ${SOURCES})

target_include_directories(${PROJECT_NAME} PRIVATE
        ${PROJECT_SOURCE_DIR}/include
)

target_link_directories(${PROJECT_NAME} PUBLIC
        ${PROJECT_SOURCE_DIR}/lib
)
