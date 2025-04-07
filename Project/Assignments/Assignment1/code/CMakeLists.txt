#cmake_minimum_required (VERSION 3.29) # 指定了CMake的最低版本要求，这里是3.29.3
project (Rasterizer) # 定义了项目名称，这里是Rasterizer。
# 这里的路径记得改成你自己的路径
set(OpenCV_DIR F:/OpenCV-MinGW-Build-OpenCV-4.5.5-x64)  # OpenCV路径
find_package(OpenCV REQUIRED)

set(CMAKE_CXX_STANDARD 17)

# mingw32-make install命令执行后安装到了c盘Program File x86
# 大概率是一样的路径 
include_directories("F:/Eigen3/include/eigen3")

add_executable(Rasterizer main.cpp rasterizer.hpp rasterizer.cpp Triangle.hpp Triangle.cpp)
target_link_libraries(Rasterizer ${OpenCV_LIBRARIES})