cmake_minimum_required(VERSION 3.0)

project(mpc)

set(SOURCES
    mpc.c
    mpc.h)

add_library(mpc STATIC ${SOURCES})

target_compile_options(mpc PRIVATE
    -pedantic -O3 -g -Wall -Werror -Wextra -Wformat=2 -Wshadow
    -Wno-long-long -Wno-overlength-strings -Wno-format-nonliteral -Wcast-align
    -Wwrite-strings -Wstrict-prototypes -Wold-style-definition -Wredundant-decls
    -Wnested-externs -Wmissing-include-dirs -Wswitch-default)
