cmake_minimum_required(VERSION 2.8)

option(USE_STATIC_ESP_PGMSPACE_LIBRARY "Build esp-pgmspace static library." OFF)
option(USE_OBJECT_ESP_PGMSPACE_LIBRARY "Build esp-pgmspace object library." ON)

if (USE_OBJECT_ESP_PGMSPACE_LIBRARY)
    add_library(esp-pgmspace-object OBJECT pgmspace.c)
endif(USE_OBJECT_ESP_PGMSPACE_LIBRARY)

if (USE_STATIC_ESP_PGMSPACE_LIBRARY)
    add_library(esp-pgmspace-static STATIC pgmspace.c)
endif(USE_STATIC_ESP_PGMSPACE_LIBRARY)
