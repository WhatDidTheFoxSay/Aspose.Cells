cmake_minimum_required(VERSION 3.16)

project("Aspose.Cells")

#project("aspose-cells")


if (WIN32)
  if (CMAKE_SIZEOF_VOID_P EQUAL "8")
    set(PLATFORM "x86_64")
  else()
    set(PLATFORM "x86")
  endif()
endif()

message(STATUS "portfile-CMAKE_SIZEOF_VOID_P = ${CMAKE_SIZEOF_VOID_P}")
message(STATUS "portfile-CMAKE_CL_64 = ${CMAKE_CL_64}")
message(STATUS "portfile-CMAKE_SYSTEM_NAME = ${CMAKE_SYSTEM_NAME}")
message(STATUS "portfile-CMAKE_TOOLCHAIN_FILE = ${CMAKE_TOOLCHAIN_FILE}")

message(STATUS "portfile-PLATFORM = ${PLATFORM}")


install(FILES "${CMAKE_CURRENT_LIST_DIR}/lib/win_${PLATFORM}/Aspose.Cells.lib" DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
install(FILES "${CMAKE_CURRENT_LIST_DIR}/lib/win_${PLATFORM}/Aspose.Cells.dll" DESTINATION ${CMAKE_CURRENT_BINARY_DIR})


message(STATUS "cmakelist-CMAKE_CURRENT_SOURCE_DIR = ${CMAKE_CURRENT_SOURCE_DIR}")
message(STATUS "cmakelist-CMAKE_INSTALL_INCLUDEDIR = ${CMAKE_INSTALL_INCLUDEDIR}")
message(STATUS "cmakelist-CMAKE_CURRENT_BINARY_DIR = ${CMAKE_CURRENT_BINARY_DIR}")

message(STATUS "cmakelist-CMAKE_CURRENT_LIST_DIR = ${CMAKE_CURRENT_LIST_DIR}")

message(STATUS "cmakelist-CMAKE_INSTALL_BINDIR = ${CMAKE_INSTALL_BINDIR}")
message(STATUS "cmakelist-CMAKE_INSTALL_LIBDIR = ${CMAKE_INSTALL_BINDIR}")
message(STATUS "cmakelist-CMAKE_INSTALL_INCLUDEDIR = ${CMAKE_INSTALL_BINDIR}")
message(STATUS "cmakelist-CMAKE_INSTALL_INCLUDEDIR = ${CMAKE_INSTALL_INCLUDEDIR}")



install(DIRECTORY  ${CMAKE_CURRENT_LIST_DIR}/include/ DESTINATION include)

install(FILES "${CMAKE_CURRENT_LIST_DIR}/aspose.cells.cpp.targets" DESTINATION share/Aspose.Cells)
install(FILES "${CMAKE_CURRENT_LIST_DIR}/aspose.cells-config.cmake" DESTINATION share/Aspose.Cells)
