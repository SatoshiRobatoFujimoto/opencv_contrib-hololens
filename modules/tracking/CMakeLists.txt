set(the_description "Tracking API")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

ocv_define_module(tracking opencv_imgproc opencv_core opencv_video opencv_highgui opencv_plot OPTIONAL opencv_datasets WRAP python)
