cmake_minimum_required(VERSION 3.0.0)

set(CMAKE_DIR "${CMAKE_CURRENT_LIST_DIR}/cmake" CACHE PATH "The path to the cmake directory")
list(APPEND CMAKE_MODULE_PATH ${CMAKE_DIR})
set(GROUP_SIG_DIR "${CMAKE_CURRENT_LIST_DIR}" CACHE PATH "Path to the root directory for group sig")


include(CompilerSettings)
include(ProjectBoost)
include(ProjectCryptopp)
include(ProjectPbc)
include(ProjectPbcSig)
find_package(Dev)
find_package(GMP REQUIRED)

include_directories(${JSONCPP_INCLUDE_DIRS})
include_directories(${GROUP_SIG_INCLUDE_DIRS})
include_directories(${CRYPTOPP_INCLUDE_DIR})

add_subdirectory(devcore)
add_subdirectory(algorithm)
