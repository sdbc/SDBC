CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(socket C)

SET(CMAKE_BUILD_TYPE type_of_build)
SET(CMAKE_C_FLAGS "-Werror -O3 -m64 -fPIC -g")

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/../include ${PROJECT_SOURCE_DIR})

SET(SRC_LIST freevar.c gethostaddr.c net_pkg.c AIO_tcp.c tcpopen.c)

ADD_LIBRARY(${PROJECT_NAME} STATIC ${SRC_LIST})
