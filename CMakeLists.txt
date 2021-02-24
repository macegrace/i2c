project(fit)
cmake_minimum_required(VERSION 3.11)

SET(GCC_COVERAGE_LINK_FLAGS    "-l bcm2835")

add_definitions(${GCC_COVERAGE_LINK_FLAGS})

set(${PROJECT_NAME}_sources src/proj1.c)
set(${PROJECT_NAME}_headers)

add_executable(${PROJECT_NAME}
        ${${PROJECT_NAME}_sources}
        ${${PROJECT_NAME}_headers}
)

target_include_directories(${PROJECT_NAME} PRIVATE include)

install(TARGETS ${PROJECT_NAME} DESTINATION /usr/bin/)
