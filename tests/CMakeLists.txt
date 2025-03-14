add_executable(test1 test1.cpp)
target_link_libraries(test1 ${ALL_LIBS})
add_test(NAME test1 COMMAND $<TARGET_FILE:test1>)
#add_test(test_foo test_foo)

add_executable(test2_mem_store test2_mem_store.cpp)
target_link_libraries(test2_mem_store ${ALL_LIBS})
add_test(NAME test2_mem_store COMMAND $<TARGET_FILE:test2_mem_store>)

add_executable(test2_mem_windowed_store test2_mem_windowed_store.cpp)
target_link_libraries(test2_mem_windowed_store ${ALL_LIBS})
add_test(NAME test2_mem_windowed_store COMMAND $<TARGET_FILE:test2_mem_windowed_store>)

add_executable(test2_mem_counter_store test2_mem_counter_store.cpp)
target_link_libraries(test2_mem_counter_store ${ALL_LIBS})
add_test(NAME test2_mem_counter_store COMMAND $<TARGET_FILE:test2_mem_counter_store>)

if (ENABLE_ROCKSDB)
    add_executable(test2_rocksdb_store test2_rocksdb_store.cpp)
    target_link_libraries(test2_rocksdb_store ${ALL_LIBS})
    add_test(NAME test2_rocksdb_store COMMAND $<TARGET_FILE:test2_rocksdb_store>)

    add_executable(test2_rocksdb_windowed_store test2_rocksdb_windowed_store.cpp)
    target_link_libraries(test2_rocksdb_windowed_store ${ALL_LIBS})
    add_test(NAME test2_rocksdb_windowed_store COMMAND $<TARGET_FILE:test2_rocksdb_windowed_store>)

    add_executable(test2_rocksdb_counter_store test2_rocksdb_counter_store.cpp)
    target_link_libraries(test2_rocksdb_counter_store ${ALL_LIBS})
    add_test(NAME test2_rocksdb_counter_store COMMAND $<TARGET_FILE:test2_rocksdb_counter_store>)
endif ()

add_executable(test3_mem_token_bucket test3_mem_token_bucket.cpp)
target_link_libraries(test3_mem_token_bucket ${ALL_LIBS})
add_test(NAME test3_mem_token_bucket COMMAND $<TARGET_FILE:test3_mem_token_bucket>)

add_executable(test4_kafka_consumer test4_kafka_consumer.cpp)
target_link_libraries(test4_kafka_consumer ${ALL_LIBS})
add_test(NAME test4_kafka_consumer COMMAND $<TARGET_FILE:test4_kafka_consumer>)

add_executable(test5_kafka_source_sink test5_kafka_source_sink.cpp)
target_link_libraries(test5_kafka_source_sink ${ALL_LIBS})
add_test(NAME test5_kafka_source_sink COMMAND $<TARGET_FILE:test5_kafka_source_sink>)

add_executable(test6_repartition test6_repartition.cpp)
target_link_libraries(test6_repartition ${ALL_LIBS})
add_test(NAME test6_repartition COMMAND $<TARGET_FILE:test6_repartition>)

add_executable(test7_cluster_uri test7_cluster_uri.cpp)
target_link_libraries(test7_cluster_uri ${ALL_LIBS})
add_test(NAME test7_cluster_uri COMMAND $<TARGET_FILE:test7_cluster_uri>)

add_executable(test7_url_vector test7_url_vector.cpp)
target_link_libraries(test7_url_vector ${ALL_LIBS})
add_test(NAME test7_url_vector COMMAND $<TARGET_FILE:test7_url_vector>)


add_executable(test8_join test8_join.cpp)
target_link_libraries(test8_join ${ALL_LIBS})
add_test(NAME test8_join COMMAND $<TARGET_FILE:test8_join>)

#add_executable(test9_kafka_rest test9_kafka_rest.cpp)
#target_link_libraries(test9_kafka_rest ${CSI_LIBS_STATIC})
#add_test(NAME test9_kafka_rest COMMAND $<TARGET_FILE:test9_kafka_rest>)

add_executable(test10_http test10_http.cpp)
target_link_libraries(test10_http ${ALL_LIBS})
add_test(NAME test10_http COMMAND $<TARGET_FILE:test10_http>)


add_executable(test11_metrics test11_metrics.cpp)
target_link_libraries(test11_metrics ${ALL_LIBS})
add_test(NAME test11_metrics COMMAND $<TARGET_FILE:test11_metrics>)

if (ENABLE_S3)
    add_executable(test12_s3 test12_s3.cpp)
    target_link_libraries(test12_s3 ${ALL_LIBS})
    add_test(NAME test12_s3 COMMAND $<TARGET_FILE:test12_s3>)
endif ()

add_executable(test13_mem test13_mem.cpp)
target_link_libraries(test13_mem ${ALL_LIBS})
add_test(NAME test13_mem COMMAND $<TARGET_FILE:test13_mem>)

add_executable(test14_async test14_async.cpp)
target_link_libraries(test14_async ${ALL_LIBS})
add_test(NAME test14_async COMMAND $<TARGET_FILE:test14_async>)

