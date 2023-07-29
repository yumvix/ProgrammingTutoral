# CMAKE_INSTALL_PREFIX not work - Solved

zlib
```cmake
project(zlib C)

#works for cmake version 3.26.3
IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
    SET(CMAKE_INSTALL_PREFIX "./Install" CACHE PATH "Installation path" FORCE)
ENDIF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)


#not works for cmake version 3.26.3
set(CMAKE_INSTALL_PREFIX, "./Install" CACHE PATH "Installation path" FORCE)
```
---
libzip
```cmake
cmake -DCMAKE_PREFIX_PATH="C://zlib" -DCMAKE_LIBRARY_PATH="C://zlib/lib" ..
```
