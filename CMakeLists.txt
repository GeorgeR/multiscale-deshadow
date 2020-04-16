cmake_minimum_required (VERSION 3.8)

set (OpenCV_DIR "C:\\Program Files\\opencv\\build")
project ("multiscale-deshadow")

find_package(OpenCV REQUIRED)

add_executable (multiscale-deshadow "multiscale-deshadow.cpp" "multiscale-deshadow.h" "shadow_remove.cpp" "smooth_detail.cpp")

link_directories(${OpenCV_LIB_DIR})
target_link_libraries(multiscale-deshadow ${OpenCV_LIBS})