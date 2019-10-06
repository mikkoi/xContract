add_executable(test.scratch.test1 test.scratch.test1.cpp)
target_link_libraries(test.scratch.test1 xContract STLSoft::STLSoft)
add_test(test.scratch.test1 ./test.scratch.test1)

