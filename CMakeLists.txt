cmake_minimum_required (VERSION 2.6)
project (ctests)
set (ctests_VERSION_MAJOR 1)
set (ctests_VERSION_MINOR 0)

configure_file ( "${PROJECT_SOURCE_DIR}/ctestsconfig.h.in" "${PROJECT_BINARY_DIR}/ctestsconfig.h" )
include_directories("${PROJECT_BINARY_DIR}")
option(USE_MYLIB "use my library functions" ON)
if(USE_MYLIB)
include_directories("${PROJECT_SOURCE_DIR}/MyLibrary")
add_subdirectory(MyLibrary)
set (EXTRA_LIBS ${EXTRA_LIBS} MyLibrary)
endif(USE_MYLIB)
add_executable(ctests main.c)
target_link_libraries(ctests ${EXTRA_LIBS})
install (TARGETS ctests DESTINATION bin)
install (FILES "${PROJECT_BINARY_DIR}/ctestsconfig.h" DESTINATION include)

include(CTest)
add_test(ctestsRuns ctests "")
add_test(ctestsConstructor ctests "")
set_tests_properties(ctestsConstructor PROPERTIES PASS_REGULAR_EXPRESSION "Default constructor called")

include (InstallRequiredSystemLibraries)
set (CPACK_RESOURCE_FILE_LICENSE  
     "${CMAKE_CURRENT_SOURCE_DIR}/License.txt")
set (CPACK_PACKAGE_VERSION_MAJOR "${ctests_VERSION_MAJOR}")
set (CPACK_PACKAGE_VERSION_MINOR "${ctests_VERSION_MINOR}")
include (CPack)


