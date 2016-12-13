## 作者
    hanfeng

## 使用方法
### (1).准备条件
   模块 - MySQLDB     
   Python版本 >= 2.6.x (3.x版本没测试)
### (2).调用方法
    Usage:
    ./mysql_innodb_status.py -h <database_ip> -u <username> -p <password>
    -h : database ip address/domain name
    -u : username
    -p : password
### (3).输出结构
    程序返回为如下结构体，可在自己代码中直接调用即可。 
    
    RETURN STRUCTURE
        {
            'section':
            {
                'key':{'val':'xxx','unit':'xxx'}
            }
        }
        example:
        {
            'bufferpool_memory': 
            {
                'buffer_pool_size': {'unit': 'BYTE', 'val': '32768'},
                'database_pages': {'unit': 'PAGE', 'val': '9484'},
                'dictionary_memory_allocated': {'unit': 'BYTE'}
            }
        }
## 输出示例
    [ background_thread ]
    --------------------------------------------------------------------------------
    master_thread_log_flush_and_writes                      26579             NUM
    master_thread_loops_active                                445             NUM
    master_thread_loops_idle                                26134             NUM
    master_thread_loops_shutdown                                0             NUM

    [ bufferpool_memory ]
    --------------------------------------------------------------------------------
    buffer_pool_size                                        32764             NUM
    database_pages                                           2635            PAGE
    dictionary_memory_allocated                            365465            BYTE
    evicted_without_access                                   0.00      PER_SECOND
    free_buffers                                            30117             NUM
    lrn_len                                                  2635             NUM
    modified_db_pages                                           0            PAGE
    old_database_pages                                        957            PAGE
    pages_created                                              73             NUM
    pages_made_non_young_per_sec                             0.00      PER_SECOND
    pages_made_not_young                                        0             NUM
    pages_made_young                                           21             NUM
    pages_made_young_per_sec                                 0.00      PER_SECOND
    pages_read                                               2562             NUM
    pages_read_ahead                                         0.00      PER_SECOND
    pages_written                                            5148             NUM
    pending_writes_flush_list                                   0             NUM
    pending_writes_lru                                          0             NUM
    pending_writes_single_page                                  0             NUM
    random_read_ahead                                        0.00      PER_SECOND
    total_large_memory_allocated                        549715968            BYTE
    unzip_lru_len                                               0             NUM

    [ file_io ]
    --------------------------------------------------------------------------------
    avg_bytes_per_read                                          0            BYTE
    fsyncs_per_second                                        0.00             NUM
    os_file_reads                                            2593             NUM
    os_file_writes                                         118211             NUM
    os_fsyncs                                                1973             NUM
    reads_per_second                                         0.00             NUM
    writes_per_second                                        0.00             NUM

    [ insert_buffer_adaptive_hash_index ]
    --------------------------------------------------------------------------------
    discarded_operations_delete                                 0             NUM
    discarded_operations_delete_mark                            0             NUM
    discarded_operations_insert                                 0             NUM
    hash_searches_per_second                                 0.00      PER_SECOND
    ibuf_free_list_len                                          0             NUM
    ibuf_merges                                                 0             NUM
    ibuf_seg_size                                               2             NUM
    ibuf_size                                                   1             NUM
    merged_operations_delete                                    0             NUM
    merged_operations_delete_mark                               0             NUM
    merged_operations_insert                                    0             NUM
    non_hash_searches_per_second                             0.00      PER_SECOND

    [ log ]
    --------------------------------------------------------------------------------
    last_checkpoint_at                                 1444180670             NUM
    log_flushed_up_to                                  1444180679             NUM
    log_ios_done                                           112643             NUM
    log_sequence_number                                1444180679             NUM
    pages_flushed_up_to                                1444180679             NUM
    pending_chkp_writes                                         0             NUM
    pending_log_flushes                                         0             NUM

    [ row_operations ]
    --------------------------------------------------------------------------------
    deletes_per_second                                       0.00             NUM
    inserts_per_second                                       0.00             NUM
    number_of_rows_deleted                                 129117             NUM
    number_of_rows_inserted                                129117             NUM
    number_of_rows_read                                  54637053             NUM
    number_of_rows_updated                                 388671             NUM
    queries_inside_innodb                                       0             NUM
    read_views_open_inside_innodb                               0             NUM
    reads_per_second                                         0.00             NUM
    updates_per_second                                       0.00             NUM

    [ semaphores ]
    --------------------------------------------------------------------------------
    reservation_count                                      116821             NUM
    rw_excl_os_waits                                        10287             NUM
    rw_excl_rounds                                         139507             NUM
    rw_excl_spins                                               0             NUM
    rw_shared_os_waits                                      13124             NUM
    rw_shared_rounds                                        53483             NUM
    rw_shared_spins                                             0             NUM
    rw_sx_os_waits                                             25             NUM
    rw_sx_rounds                                              750             NUM
    rw_sx_spins                                                25             NUM
    signal_count                                           116126             NUM
    spin_rounds_per_wait_rw_excl                        139507.00             NUM
    spin_rounds_per_wait_rw_shared                       53483.00             NUM
    spin_rounds_per_wait_rw_sx                              30.00             NUM

    [ transactions ]
    --------------------------------------------------------------------------------
    history_list_length                                       633             NUM
    purge_done_for_trx                                    1126318             NUM
    purge_done_for_undo                                         0             NUM
    trx_counter                                           1126318             NUM
