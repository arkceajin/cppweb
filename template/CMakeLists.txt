project(cmake)
cmake_minimum_required(VERSION 2.6)
aux_source_directory(. SRC_LIST)
if (DEFINED ENV{OPENSHIFT_APP_NAME})
    add_executable($ENV{OPENSHIFT_APP_NAME}_exec ${SRC_LIST})
else()
    add_executable(${PROJECT_NAME} ${SRC_LIST})
endif()


