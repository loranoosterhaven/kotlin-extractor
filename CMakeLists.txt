cmake_minimum_required(VERSION 3.15)
project(src)

set(CMAKE_CXX_STANDARD 14)

# add extra include directories
include_directories(/usr/local/include)

# add extra lib directories
link_directories(/usr/local/lib)

add_executable(src main.cpp directory.h directory.cpp apk.cpp apk.h dex.cpp dex.h kotlininspector.cpp kotlininspector.h kotlinanalyzer.cpp kotlinanalyzer.h dextypes.h bytepattern.cpp bytepattern.h disassembler.cpp disassembler.h csvwriter.cpp csvwriter.h axml_parser/axml_parser.cpp axml_parser/axml_parser.hpp axml_parser/stream_reader.hpp)

# specify the dependency on an extra library
target_link_libraries(src libzip.a)

# Boost.
set(BOOST_MIN_VERSION "1.53.0")
find_package(Boost ${BOOST_MIN_VERSION}
        COMPONENTS system iostreams program_options locale REQUIRED)
include_directories(SYSTEM ${Boost_INCLUDE_DIRS})
add_definitions(
        -DBOOST_MAJOR_VERSION=${Boost_MAJOR_VERSION}
        -DBOOST_MINOR_VERSION=${Boost_MINOR_VERSION}
)
target_link_libraries(src ${Boost_LIBRARIES})