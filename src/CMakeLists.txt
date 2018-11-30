CMAKE_MINIMUM_REQUIRED(VERSION 2.10.1)

aux_source_directory(. DIR_RTKLIB_SRC)
aux_source_directory(./rcv DIR_RTKLIB_SRC_RCV)
list(APPEND DIR_RTKLIB_SRC ${DIR_RTKLIB_SRC_RCV})

link_libraries(-lpthread -lm)

include_directories(../../iot_tel[)
include_directories(../../azure_iot_sdk_c/iothub_client/inc)

add_library(rtklib ${DIR_RTKLIB_SRC})
target_link_libraries(rtklib iot_tel)
