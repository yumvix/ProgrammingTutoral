# CMAKE_INSTALL_PREFIX not work

```cmake
project(zlib C)

#works for cmake version 3.26.3
IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
    SET(CMAKE_INSTALL_PREFIX "./Install" CACHE PATH "Installation path" FORCE)
ENDIF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)


#not works for cmake version 3.26.3
set(CMAKE_INSTALL_PREFIX, "./Install" CACHE PATH "Installation path" FORCE)
```
