cmake_minimum_required(VERSION 3.23)
project(Sandworm)

set(CMAKE_CXX_STANDARD 14)

include_directories(Sandworm/Include)

include_directories(/opt/homebrew/Cellar/llvm/14.0.6_1/include)
link_libraries(
        /opt/homebrew/Cellar/llvm/14.0.6_1/lib/libLLVM-14.dylib
        /opt/homebrew/Cellar/llvm/14.0.6_1/lib/libclang.dylib
        /opt/homebrew/Cellar/llvm/14.0.6_1/lib/libclang-cpp.dylib
)

add_executable(Sandworm
        Example/main.cpp
        Sandworm/Include/Sandworm.h
        Sandworm/Source/Sandworm.cpp)
