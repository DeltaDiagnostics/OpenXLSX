#=======================================================================================================================
# Preamble
#=======================================================================================================================
cmake_minimum_required(VERSION 3.15 FATAL_ERROR)
project(OpenXLSX.Benchmark)

#=======================================================================================================================
# Set up Google Benchmark
#=======================================================================================================================
find_package(benchmark REQUIRED)

set(BENCHMARK_ENABLE_TESTING OFF)
#add_subdirectory(gbench)

#=======================================================================================================================
# Define Benchmark targets
#=======================================================================================================================
add_executable(OpenXLSXBenchmark EXCLUDE_FROM_ALL Benchmark.cpp)
target_link_libraries(OpenXLSXBenchmark PRIVATE benchmark::benchmark benchmark::benchmark_main OpenXLSX::OpenXLSX)
