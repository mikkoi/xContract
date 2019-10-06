add_executable(test.unit.violations test.unit.violations.cpp)
target_link_libraries(test.unit.violations xContract xTests::xTests STLSoft::STLSoft)
add_test(test.unit.violations ./test.unit.violations)


