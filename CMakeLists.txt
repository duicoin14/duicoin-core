cmake_minimum_required(VERSION 3.10)
project(duicoin-core VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Main executable
add_executable(duicoind 
    src/main.cpp
)

# Libraries
add_library(duicoin-core
    src/core/blockchain.cpp
    src/crypto/hash.cpp
    src/p2p/network.cpp
    src/rpc/server.cpp
)

target_link_libraries(duicoind duicoin-core)