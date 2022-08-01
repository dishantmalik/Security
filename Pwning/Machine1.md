
Host IP Address: 10.10.11.170


# Recon:

 #1 Ping test

> ping 10.10.11.170

64 bytes from 10.10.11.170: icmp_seq=0 ttl=63 time=122.715 ms
64 bytes from 10.10.11.170: icmp_seq=1 ttl=63 time=126.750 ms

this indicates that the host hasn't disabled ICMP Echo requests.

#2 Nmap
  
  nmap 
- To understand the topology of the target network/machine
- Can be used for network mapping or port scanning

Command: nmap -O -sS -sV -sC 10.10.11.170
  
  Results:
/*
Starting Nmap 7.92 ( https://nmap.org ) at 2022-08-01 15:58 CDT
Nmap scan report for 10.10.11.170
Host is up (0.12s latency).
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE    VERSION
22/tcp   open  ssh        OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 48:ad:d5:b8:3a:9f:bc:be:f7:e8:20:1e:f6:bf:de:ae (RSA)
|   256 b7:89:6c:0b:20:ed:49:b2:c1:86:7c:29:92:74:1c:1f (ECDSA)
|_  256 18:cd:9d:08:a6:21:a8:b8:b6:f7:9f:8d:40:51:54:fb (ED25519)
8080/tcp open  http-proxy
|_http-title: Red Panda Search | Made with Spring Boot
|_http-open-proxy: Proxy might be redirecting requests
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.1 200 
|     Content-Type: text/html;charset=UTF-8
|     Content-Language: en-US
|     Date: Mon, 01 Aug 2022 20:58:49 GMT
|     Connection: close
|     <!DOCTYPE html>
|     <html lang="en" dir="ltr">
|     <head>
|     <meta charset="utf-8">
|     <meta author="wooden_k">
|     <!--Codepen by khr2003: https://codepen.io/khr2003/pen/BGZdXw -->
|     <link rel="stylesheet" href="css/panda.css" type="text/css">
|     <link rel="stylesheet" href="css/main.css" type="text/css">
|     <title>Red Panda Search | Made with Spring Boot</title>
|     </head>
|     <body>
|     <div class='pande'>
|     <div class='ear left'></div>
|     <div class='ear right'></div>
|     <div class='whiskers left'>
|     <span></span>
|     <span></span>
|     <span></span>
|     </div>
|     <div class='whiskers right'>
|     <span></span>
|     <span></span>
|     <span></span>
|     </div>
|     <div class='face'>
|     <div class='eye
|   HTTPOptions: 
|     HTTP/1.1 200 
|     Allow: GET,HEAD,OPTIONS
|     Content-Length: 0
|     Date: Mon, 01 Aug 2022 20:58:49 GMT
|     Connection: close
|   RTSPRequest: 
|     HTTP/1.1 400 
|     Content-Type: text/html;charset=utf-8
|     Content-Language: en
|     Content-Length: 435
|     Date: Mon, 01 Aug 2022 20:58:50 GMT
|     Connection: close
|     <!doctype html><html lang="en"><head><title>HTTP Status 400 
|     Request</title><style type="text/css">body {font-family:Tahoma,Arial,sans-serif;} h1, h2, h3, b {color:white;background-color:#525D76;} h1 {font-size:22px;} h2 {font-size:16px;} h3 {font-size:14px;} p {font-size:12px;} a {color:black;} .line {height:1px;background-color:#525D76;border:none;}</style></head><body><h1>HTTP Status 400 
|_    Request</h1></body></html>
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port8080-TCP:V=7.92%I=7%D=8/1%Time=62E83E8A%P=x86_64-apple-darwin21.5.0
SF:%r(GetRequest,690,"HTTP/1\.1\x20200\x20\r\nContent-Type:\x20text/html;c
SF:harset=UTF-8\r\nContent-Language:\x20en-US\r\nDate:\x20Mon,\x2001\x20Au
SF:g\x202022\x2020:58:49\x20GMT\r\nConnection:\x20close\r\n\r\n<!DOCTYPE\x
SF:20html>\n<html\x20lang=\"en\"\x20dir=\"ltr\">\n\x20\x20<head>\n\x20\x20
SF:\x20\x20<meta\x20charset=\"utf-8\">\n\x20\x20\x20\x20<meta\x20author=\"
SF:wooden_k\">\n\x20\x20\x20\x20<!--Codepen\x20by\x20khr2003:\x20https://c
SF:odepen\.io/khr2003/pen/BGZdXw\x20-->\n\x20\x20\x20\x20<link\x20rel=\"st
SF:ylesheet\"\x20href=\"css/panda\.css\"\x20type=\"text/css\">\n\x20\x20\x
SF:20\x20<link\x20rel=\"stylesheet\"\x20href=\"css/main\.css\"\x20type=\"t
SF:ext/css\">\n\x20\x20\x20\x20<title>Red\x20Panda\x20Search\x20\|\x20Made
SF:\x20with\x20Spring\x20Boot</title>\n\x20\x20</head>\n\x20\x20<body>\n\n
SF:\x20\x20\x20\x20<div\x20class='pande'>\n\x20\x20\x20\x20\x20\x20<div\x2
SF:0class='ear\x20left'></div>\n\x20\x20\x20\x20\x20\x20<div\x20class='ear
SF:\x20right'></div>\n\x20\x20\x20\x20\x20\x20<div\x20class='whiskers\x20l
SF:eft'>\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20<span></span>\n\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20<span></span>\n\x20\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20<span></span>\n\x20\x20\x20\x20\x20\x20</div>\n\x20\x20\
SF:x20\x20\x20\x20<div\x20class='whiskers\x20right'>\n\x20\x20\x20\x20\x20
SF:\x20\x20\x20<span></span>\n\x20\x20\x20\x20\x20\x20\x20\x20<span></span
SF:>\n\x20\x20\x20\x20\x20\x20\x20\x20<span></span>\n\x20\x20\x20\x20\x20\
SF:x20</div>\n\x20\x20\x20\x20\x20\x20<div\x20class='face'>\n\x20\x20\x20\
SF:x20\x20\x20\x20\x20<div\x20class='eye")%r(HTTPOptions,75,"HTTP/1\.1\x20
SF:200\x20\r\nAllow:\x20GET,HEAD,OPTIONS\r\nContent-Length:\x200\r\nDate:\
SF:x20Mon,\x2001\x20Aug\x202022\x2020:58:49\x20GMT\r\nConnection:\x20close
SF:\r\n\r\n")%r(RTSPRequest,24E,"HTTP/1\.1\x20400\x20\r\nContent-Type:\x20
SF:text/html;charset=utf-8\r\nContent-Language:\x20en\r\nContent-Length:\x
SF:20435\r\nDate:\x20Mon,\x2001\x20Aug\x202022\x2020:58:50\x20GMT\r\nConne
SF:ction:\x20close\r\n\r\n<!doctype\x20html><html\x20lang=\"en\"><head><ti
SF:tle>HTTP\x20Status\x20400\x20\xe2\x80\x93\x20Bad\x20Request</title><sty
SF:le\x20type=\"text/css\">body\x20{font-family:Tahoma,Arial,sans-serif;}\
SF:x20h1,\x20h2,\x20h3,\x20b\x20{color:white;background-color:#525D76;}\x2
SF:0h1\x20{font-size:22px;}\x20h2\x20{font-size:16px;}\x20h3\x20{font-size
SF::14px;}\x20p\x20{font-size:12px;}\x20a\x20{color:black;}\x20\.line\x20{
SF:height:1px;background-color:#525D76;border:none;}</style></head><body><
SF:h1>HTTP\x20Status\x20400\x20\xe2\x80\x93\x20Bad\x20Request</h1></body><
SF:/html>");
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.92%E=4%D=8/1%OT=22%CT=1%CU=31451%PV=Y%DS=2%DC=I%G=Y%TM=62E83EA9
OS:%P=x86_64-apple-darwin21.5.0)SEQ(SP=101%GCD=1%ISR=106%TI=Z%CI=Z%TS=A)SEQ
OS:(SP=101%GCD=1%ISR=106%TI=Z%CI=Z%II=I%TS=C)SEQ(CI=Z)SEQ(CI=Z%II=I)OPS(O1=
OS:M550ST11NW7%O2=M550ST11NW7%O3=M550NNT11NW7%O4=M550ST11NW7%O5=M550ST11NW7
OS:%O6=M550ST11)WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y
OS:%DF=Y%T=40%W=FAF0%O=M550NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD
OS:=0%Q=)T2(R=N)T3(R=N)T4(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T5(R=Y%D
OS:F=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O
OS:=%RD=0%Q=)T7(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%T=40
OS:%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Network Distance: 2 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 41.20 seconds
*/

Results:

2 ports are open:
22 - for SSH
8080 - HTTP Proxy
