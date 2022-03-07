# Webbench测试

## 测试前须知

Webbench只能对WebServer压测，无法对网络库压测。

Webbench返回结果是每分钟响应请求数（QPS是每秒响应请求数）和每秒传输数据量（吞吐量）。

最好和其他http服务器对比，在跑满CPU的情况下，对比吞吐量。

## 测试一



```shell
root@ubuntu:~/project/webserver/version_1/test_presure/webbench-1.5# ./webbench -t 5 -c 1000 http://192.168.1.1:9999/
Webbench - Simple Web Benchmark 1.5
Copyright (c) Radim Kolar 1997-2004, GPL Open Source Software.

Benchmarking: GET http://192.168.1.1:9999/
1000 clients, running 5 sec.

Speed=292860 pages/min, 546672 bytes/sec.
Requests: 24405 susceed, 0 failed.
```

# 测试二

```shell
root@ubuntu:~/project/webserver/version_1/test_presure/webbench-1.5# ./webbench -t 5 -c 9000 http://192.168.1.1:9999/
Webbench - Simple Web Benchmark 1.5
Copyright (c) Radim Kolar 1997-2004, GPL Open Source Software.

Benchmarking: GET http://192.168.1.1:9999/
9000 clients, running 5 sec.

Speed=286944 pages/min, 535651 bytes/sec.
Requests: 23912 susceed, 0 failed.
```

