# echoserver

A tcp echo server to validate tcp routing 

```
cf push echoserver -d tcp.haas-22.shaozhenpcf.com --random-route -b go_buildpack
```

```
cf app echoserver
Showing health and status for app echoserver in org test-org / space test-space as admin...
OK

requested state: started
instances: 1/1
usage: 1G x 1 instances
urls: tcp.haas-22.shaozhenpcf.com:4511, tcp.haas-22.shaozhenpcf.com:3053, tcp.haas-22.shaozhenpcf.com:1251, tcp.haas-22.shaozhenpcf.com:4414, tcp.haas-22.shaozhenpcf.com:3209, tcp.haas-22.shaozhenpcf.com:1121, tcp.haas-22.shaozhenpcf.com:4091, tcp.haas-22.shaozhenpcf.com:4679, tcp.haas-22.shaozhenpcf.com:1475
last uploaded: Fri Sep 30 18:24:10 UTC 2016
stack: cflinuxfs2
buildpack: go_buildpack

     state     since                    cpu    memory       disk         details
#0   running   2016-09-30 01:25:06 PM   0.0%   3.9M of 1G   4.8M of 1G
```

```
telnet tcp.haas-22.shaozhenpcf.com 4511
Trying 10.65.153.64...
Connected to tcp.haas-22.shaozhenpcf.com.
Escape character is '^]'.
Hello World!~
Hello World!~
```
