# MVTSO_KIDA

## How to use
- Build masstree
```
$ cd ../
$ ./bootstrap.sh
```
This makes ../third_party/masstree/libkohler_masstree_json.a used by building mvtso.
- Build mimalloc
```
$ cd ../
$ ./bootstrap_mimalloc.sh
```
This makes ../third_party/mimalloc/out/release/libmimalloc.a used by building mvtso.
- Build 
```
$ mkdir build
$ cd build
$ cmake -G Ninja -DCMAKE_BUILD_TYPE=Release ..
$ ninja
```
- Confirm usage 
```
$ ./mvtso.exe -help
```
- Execution example 
```
$ numactl --interleave=all ./mvtso.exe -tuple_num=1000 -max_ope=10 -thread_num=224 -rratio=100 -zipf_skew=0 -ycsb=1 -clocks_per_us=2100 -io_time_ns=5 -extime=3 -comm_time_ms=1 -batch_size=4 

```

