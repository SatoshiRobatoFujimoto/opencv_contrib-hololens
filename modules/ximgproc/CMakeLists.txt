set(the_description "Extended image processing module. It includes edge-aware filters and etc.")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

set(OPENCV_MODULE_IS_PART_OF_WORLD OFF)
ocv_define_module(ximgproc opencv_imgproc opencv_core opencv_highgui opencv_calib3d WRAP python)

target_link_libraries(opencv_ximgproc)
