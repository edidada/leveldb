# 我自己的编译

## compile docs

[编译测试例子](https://zhuanlan.zhihu.com/p/34657032)

按照例子，执行cmake完毕

```shell

cd /home/edidada/Project/leveldb/cmake-build-debug

make

ls

./app_test
```


[leveldb source code anynastic](https://github.com/snipercy/leveldb)


## function reference

```shell
man 3 assert
```


## unit test

```shell script
/home/edidada/Project/leveldb/cmake-build-debug/db_bench
LevelDB:    version 1.22
Date:       Thu Feb 13 21:58:42 2020
CPU:        4 * Intel(R) Core(TM) i7-5500U CPU @ 2.40GHz
CPUCache:   4096 KB
Keys:       16 bytes each
Values:     100 bytes each (50 bytes after compression)
Entries:    1000000
RawSize:    110.6 MB (estimated)
FileSize:   62.9 MB (estimated)
WARNING: Optimization is disabled: benchmarks unnecessarily slow
WARNING: Assertions are enabled; benchmarks unnecessarily slow
WARNING: Snappy compression is not enabled
------------------------------------------------
... finished 1000000 ops                              fillseq      :       7.766 micros/op;   14.2 MB/s
... finished 1000 ops                              fillsync     :   29801.754 micros/op;    0.0 MB/s (1000 ops)
... finished 1000 ops                              fillrandom   :      15.877 micros/op;    7.0 MB/s
... finished 800 ops                              overwrite    :      24.464 micros/op;    4.5 MB/s
... finished 2000 ops                              readrandom   :      11.944 micros/op; (1000000 of 1000000 found)
... finished 30000 ops                              readrandom   :       8.813 micros/op; (1000000 of 1000000 found)
... finished 15000 ops                              readseq      :       0.688 micros/op;  160.7 MB/s
... finished 600000 ops                              readreverse  :       1.310 micros/op;   84.5 MB/s
compact      : 3166916.000 micros/op;
... finished 35000 ops                              readrandom   :       4.961 micros/op; (1000000 of 1000000 found)
... finished 15000 ops                              readseq      :       0.495 micros/op;  223.4 MB/s
... finished 600000 ops                              readreverse  :       0.993 micros/op;  111.4 MB/s
... finished 1000 ops                              fill100K     :    5659.964 micros/op;   16.9 MB/s (1000 ops)
... crc=0xa46ab21fcrc32c       :       9.599 micros/op;  406.9 MB/s (4K per op)
snappycomp   :    7913.000 micros/op; (snappy failure)
snappyuncomp :    7366.000 micros/op; (snappy failure)

Process finished with exit code 0
```


cmake
include()语法

cmake设置软件版本
set(GOOGLETEST_VERSION 1.10.0)
project(leveldb VERSION 1.22.0 LANGUAGES C CXX)
