# Test Concurrent Requests on Reactive Spring Boot
```
➜  ~ ab -c 1000 -n 1000000 http://localhost:8080/hello
This is ApacheBench, Version 2.3 <$Revision: 1843412 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking localhost (be patient)
Completed 100000 requests
Completed 200000 requests
Completed 300000 requests
Completed 400000 requests
Completed 500000 requests
Completed 600000 requests
Completed 700000 requests
Completed 800000 requests
Completed 900000 requests
Completed 1000000 requests
Finished 1000000 requests


Server Software:        
Server Hostname:        localhost
Server Port:            8080

Document Path:          /hello
Document Length:        14 bytes

Concurrency Level:      1000
Time taken for tests:   104.164 seconds
Complete requests:      1000000
Failed requests:        0
Total transferred:      79000000 bytes
HTML transferred:       14000000 bytes
Requests per second:    9600.24 [#/sec] (mean)
Time per request:       104.164 [ms] (mean)
Time per request:       0.104 [ms] (mean, across all concurrent requests)
Transfer rate:          740.64 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    3   3.2      2      41
Processing:     0  102  51.3     94     543
Waiting:        0  100  51.4     92     543
Total:          0  104  51.2     96     543

Percentage of the requests served within a certain time (ms)
  50%     96
  66%    114
  75%    128
  80%    139
  90%    169
  95%    200
  98%    241
  99%    264
 100%    543 (longest request)

```
