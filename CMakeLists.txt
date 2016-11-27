cmake_minimum_required (VERSION 2.6)
project (BMP180-TEST)

set(CMAKE_CURRENT_SOURCE_DIR .)

SET(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)
set(CMAKE_INSTALL_PREFIX /usr/)

set(BMP180_SOURCE
  bmp180-test.cpp
)

add_executable(bmp180-test ${BMP180_SOURCE})
target_link_libraries(bmp180-test firmware_i2c bmp180)

install(TARGETS bmp180-test DESTINATION bin)
