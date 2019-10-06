add_library(xContract xcontract.core.c)
target_link_libraries(xContract STLSoft::STLSoft)
set_target_properties(xContract PROPERTIES
    OUTPUT_NAME "xcontract.core"
    PUBLIC_HEADER ${CMAKE_SOURCE_DIR}/include/xcontract/xcontract.h)
target_include_directories(xContract PUBLIC
    $<BUILD_INTERFACE:${CMAKE_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>)

install(TARGETS xContract
    EXPORT project-targets
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/xcontract
)

