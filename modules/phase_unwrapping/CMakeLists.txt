set(the_description "Phase Unwrapping API")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

ocv_define_module(phase_unwrapping opencv_core opencv_calib3d opencv_imgproc opencv_highgui opencv_features2d opencv_rgbd WRAP python java)
