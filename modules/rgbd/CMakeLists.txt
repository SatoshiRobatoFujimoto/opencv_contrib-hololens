set(the_description "RGBD algorithms")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

ocv_warnings_disable(CMAKE_CXX_FLAGS -Wundef)
ocv_define_module(rgbd opencv_core opencv_calib3d opencv_highgui opencv_imgproc WRAP python)
