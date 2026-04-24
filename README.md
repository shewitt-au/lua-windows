# Lua for Windows

The aim of this repo is to get Lua working on Windows better. It is a newborn project so not a lot has been done so far.

## What has been done?

- A solution to build Lua using Visual Studio (build-systems\visual-studio-2022)
- Improved utf8 support in the standalone interpreter

### Building

First pull the repo. Lua is included as a submodule so be sure to use the recurse submodules option:
```
git clone --recurse-submodules https://github.com/shewitt-au/lua-windows.git
```

Navigate to ".\build-systems\visual-studio-2022" and load the solution (lua.sln).

There are muplitple projects:
1. "lua_dll": lua is built as a dll
2. "lua_static": lua is built as a static library
3. "luacli_dll": the standalone interpreter using lua via a dll
4. "luacli_static": the standalone interpreter statically linking to lua

Each of these has four configurations:
1. "Debug": build a debug version using C
2. "Release": build a release version using C
3. "CPP Debug": build a debug version using CPP
4. "CPP Release": build a release version using CPP
