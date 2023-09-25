# mariadb mysql won't start
...<br>
[Note] InnoDB: Uses event mutexes<br>
[Note] InnoDB: Compressed tables use zlib 1.2.13<br>
[Note] InnoDB: Number of pools: 1<br>
[Note] InnoDB: Using generic crc32 instructions<br>
[Note] InnoDB: Initializing buffer pool, total size = 134217728, chunk size = 134217728<br>
[Note] InnoDB: Completed initialization of buffer pool<br>
[Note] InnoDB: Starting crash recovery from checkpoint LSN=45175,45175<br>
[ERROR] InnoDB: Missing FILE_CHECKPOINT at 45175 between the checkpoint 45175 and the end 45295.<br>
[ERROR] InnoDB: Plugin initialization aborted with error Generic error<br>
[Note] InnoDB: Starting shutdown...<br>
[ERROR] Plugin 'InnoDB' init function returned error.<br>
[ERROR] Plugin 'InnoDB' registration as a STORAGE ENGINE failed.<br>
[Note] Plugin 'FEEDBACK' is disabled.<br>
[ERROR] Unknown/unsupported storage engine: InnoDB<br>
[ERROR] Aborting<br>
<br>
**solve**<br>
put this line under [mysqld] section in my.cnf or server.cnf<br>
```
innodb_force_recovery=6
```
_remove or commented after its working_
