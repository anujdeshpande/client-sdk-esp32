cmake_minimum_required(VERSION 3.16)
set(COMPONENTS main)
# The unit-test-app components were removed from IDF in v6.0 (unity_test_utils
# now lives in the unity component itself)
if(EXISTS "$ENV{IDF_PATH}/tools/unit-test-app/components")
    set(EXTRA_COMPONENT_DIRS "$ENV{IDF_PATH}/tools/unit-test-app/components")
endif()
include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(test_app)
