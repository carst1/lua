cmake_minimum_required(VERSION 3.12)
project(lua VERSION 1 LANGUAGES C)

set(src_files lauxlib.h lua.h luaconf.h lualib.h
    lapi.c lauxlib.c lbaselib.c lcode.c lcorolib.c lctype.c ldblib.c ldebug.c ldo.c
    ldump.c lfunc.c lgc.c linit.c liolib.c llex.c lmathlib.c lmem.c loadlib.c lobject.c lopcodes.c
    loslib.c lparser.c lstate.c lstring.c lstrlib.c ltable.c ltablib.c ltests.c ltm.c lundump.c
    lutf8lib.c lvm.c lzio.c)

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /FS")
SET(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} /FS")

add_library(lua ${src_files})
