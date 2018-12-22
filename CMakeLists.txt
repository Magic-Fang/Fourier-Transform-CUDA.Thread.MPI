cmake_minimum_required(VERSION 2.8)
project(FT)
find_package(MPI REQUIRED)
find_package(CUDA REQUIRED)

include_directories(${MPI_INCLUDE_PATH} src)

SET(CMAKE_C_COMPILER mpicc)
SET(CMAKE_CXX_COMPILER mpicxx)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -pthread")
set(CUDA_NVCC_FLAGS -O3;-G;-g)

set(SOURCE_FILES 
src/complex.cc
src/complex.h
src/input_image.h
src/input_image.cc
 )
add_executable(MPI ${SOURCE_FILES} MPISource.cc)
add_executable(Thread ${SOURCE_FILES} ThreadSource.cc)
cuda_add_executable(Cuda CudaSource.cu)
