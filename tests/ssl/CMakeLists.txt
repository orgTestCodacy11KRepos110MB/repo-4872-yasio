set(target_name ssltest)

set (SSLTEST_SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR})
set (SSLTEST_INC_DIR ${SSLTEST_SRC_DIR}/../../)

set (SSLTEST_SRC ${SSLTEST_SRC_DIR}/main.cpp)

include_directories ("${SSLTEST_SRC_DIR}")
include_directories ("${SSLTEST_INC_DIR}")

add_executable (${target_name} ${SSLTEST_SRC}) 

# link ssl stubs
yasio_config_app_depends(${target_name})
