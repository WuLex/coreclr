cmake_minimum_required (VERSION 2.6) 
project (PInvokePassingByRefNative) 
include ("${CLR_INTEROP_TEST_ROOT}/Interop.cmake")
include_directories("..")
include_directories(${INC_PLATFORM_DIR}) 
set(SOURCES 
    PInvokePassingByRefNative.cpp 
) 
# add the executable 
add_library (PInvokePassingByRefNative SHARED ${SOURCES}) 
target_link_libraries(PInvokePassingByRefNative ${LINK_LIBRARIES_ADDITIONAL}) 
# add the install targets 
install (TARGETS PInvokePassingByRefNative DESTINATION bin) 
