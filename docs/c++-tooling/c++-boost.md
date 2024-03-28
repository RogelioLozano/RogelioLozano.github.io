---
sidebar_position: 1
---

# Instalation and use of libraries in C++

C++ is a complied language. In MacOS the g++ source code compiler is part of the GNU (GNU's not Unix, which in the beginning was used along with the Linux kernel to build the Linux Operating System) compiller collection and it comes preinstalled.  We can choose the language standard to compile against using the std parameter.

Example:

```bash
g++ -std=c++20 mergesort.cpp
```

There are other options to, for example, compile with different optimization options (sometimes useful for reverse engineering practices or assembly langauge optimizations).

To compile using non-pre-shiped headers and libraries we use CMake. For example, I installed boost using:

```bash
brew install boost
```

It got installed in **/opt/homebrew/Cellar/boost/1.84.0_1**

In C++ when we "#include" in our source code, we bringing headers defined in the std namespace or other namespaces. Those headers work as templates and the library is the file that includes the source code for the routine. So to run a program that requires both, we use:

```bash
g++ -o my_program my_program.cpp -I/usr/local/include -L/usr/local/lib -lboost_system -lboost_thread
```

In this command:

- I/usr/local/include specifies the directory containing Boost header files.
- L/usr/local/lib specifies the directory containing Boost libraries.
- lboost_system and -lboost_thread specify the Boost libraries to link against.

Note: The library names (boost_system, boost_thread, etc.) may vary depending on which Boost libraries you need for your project.

For example, a cpp source code in ... /comptetion_problems/algorithms/karatsuba

I would use the following CMakeLists file tells CMake to find Boost, include its headers, and link against its libraries.

```CMake
cmake_minimum_required(VERSION 3.5)
project(karatsuba)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find Boost
set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)
find_package(Boost 1.84.0 REQUIRED COMPONENTS system thread)

# Include Boost headers
include_directories(${Boost_INCLUDE_DIRS})

# Add your source files
add_executable(karatsuba karatsuba.cpp)  # Replace 'main.cpp' with your actual source file(s)

# Link against Boost libraries
target_link_libraries(karatsuba ${Boost_LIBRARIES})
```

To build your project using CMake, follow these steps in the terminal:

Navigate to your project directory in the terminal.
Create a build directory (you should not build in the source directory):
```bash
mkdir build
cd build
```
Run CMake from the build directory to generate build files:
cmake ..

Once CMake has generated the build files, you can build your project using your preferred build tool (e.g., make). So inside build, just type "make" and it will build the binary.








