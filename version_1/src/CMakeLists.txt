# 定义了一个SRC_LIST变量，包含了该目录下所有的源文件
aux_source_directory(. SRC_LIST)
aux_source_directory(./config CONFIG_LIST)
aux_source_directory(./http HTTP_LIST)
aux_source_directory(./log LOG_LIST)
aux_source_directory(./timer TIMER_LIST)
aux_source_directory(./webserver WEBSERVER_LIST)

# 指定生成可执行文件
add_executable(server ${SRC_LIST} ${CONFIG_LIST} ${HTTP_LIST} ${LOG_LIST} ${TIMER_LIST} ${WEBSERVER_LIST})
# 指定可执行文件链接时需要依赖的库文件
target_link_libraries(server pthread)