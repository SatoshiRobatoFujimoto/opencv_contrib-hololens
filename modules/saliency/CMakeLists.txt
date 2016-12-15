set(the_description "Saliency API")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

set(OPENCV_MODULE_IS_PART_OF_WORLD OFF)

ocv_define_module(saliency opencv_imgproc opencv_highgui opencv_features2d WRAP python)

ocv_warnings_disable(CMAKE_CXX_FLAGS -Woverloaded-virtual)
