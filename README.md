<!-- markdownlint-disable MD059 MD025  -->

# Note

This repository merges [LuaJIT/24c20c9](https://github.com/LuaJIT/LuaJIT/commit/24c20c94e7db195b640854619577441f9b4bc6be) into [WohlSoft/LuaJIT](https://github.com/WohlSoft) *(more info [here](https://github.com/LuaJIT/LuaJIT/issues/1475))*.

It currently serves a single purpose which is to integrate a clean LuaJIT CMake build with bit operator support for [YLP](https://github.com/xesdoog/YLP).

Thanks to the [WohlSoft](https://github.com/WohlSoft) for making this simple.

# Original Readme

## LuaJIT + CMake & UTF8-paths-on-Windows

There is the modified version of LuaJIT that has the next difference from the original version:

* In addition to its default GNU Make-based build, there is a CMake-based build was added
* Enforces the UTF-8 charset for file system-related functions to ensure the equal result on all supported platforms (without this addition, locale-depending ANSI charsets used on Windows) (You should specify the `-DLUAJIT_FORCE_UTF8_FOPEN=ON` CMake option to enable this feature)

If you find a bug using CMake build, please **DON'T REPORT IT TO OFFICIAL LuaJIT developers**, as they refuse to take the CMake building system support. So, you MUST verify the [latest original version](https://github.com/LuaJIT/LuaJIT) using the GNU Make-based building system to ensure that the same bug gets reproduced too:

* If the bug gets reproduced at both CMake and GNU-Make-based builds, feel free to report the bug to [official LuaJIT developers](https://github.com/LuaJIT/LuaJIT/issues).
* If the bug gets reproduced at the CMake-based build only, however, doesn't reproduce at the official GNU-Make-based build, you [should report this bug to me](https://github.com/WohlSoft/LuaJIT/issues).

# Original *ORIGINAL* readme

## README for LuaJIT 2.1

---------------------

LuaJIT is a Just-In-Time (JIT) compiler for the Lua programming language.

Project Homepage: <https://luajit.org/>

LuaJIT is Copyright (C) 2005-2025 Mike Pall.
LuaJIT is free software, released under the MIT license.
See full Copyright Notice in the COPYRIGHT file or in luajit.h.

Documentation for LuaJIT is available in HTML format.
Please point your favorite browser to:

 doc/luajit.html
