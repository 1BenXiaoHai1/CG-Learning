cmake_minimum_required (VERSION 2.8.11) # 指定了CMake的最低版本要求，这里是2.8.11。
project (Transformation) # 定义了项目名称，这里是Transformation。

find_package(Eigen3 REQUIRED) # 告诉CMake去查找名为Eigen3的软件包。
include_directories(EIGEN3_INCLUDE_DIR) # 将Eigen3库的头文件目录添加到编译器的搜索路径中。EIGEN3_INCLUDE_DIR是find_package命令找到Eigen3后设置的一个变量，它包含了Eigen3头文件的路径。
add_executable (Transformation main.cpp) # 将main.cpp文件编译成一个可执行文件，并且这个可执行文件的名称将与项目名称相同，即Transformation。
