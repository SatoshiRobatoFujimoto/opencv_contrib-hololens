set(the_description "Object detection algorithms")

if(DEFINED WINRT AND NOT DEFINED ENABLE_WINRT_MODE_NATIVE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /ZW")
endif()

ocv_define_module(xobjdetect opencv_core opencv_imgproc opencv_highgui opencv_objdetect WRAP python)
if (NOT APPLE_FRAMEWORK)
    add_subdirectory(tools)
endif()
