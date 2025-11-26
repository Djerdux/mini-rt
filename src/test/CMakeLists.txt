add_executable(minirt-test minirt_test.cpp)

find_package(OpenMP REQUIRED)
if(OpenMP_CXX_FOUND)
    target_link_libraries(minirt-test PUBLIC OpenMP::OpenMP_CXX)
endif()

target_link_libraries(minirt-test PUBLIC minirt)

#install(TARGETS minirt-test DESTINATION bin/minirt)
