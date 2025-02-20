#python #http #networking #programming 

Creating the server from terminal

Linux
```python
$ python3 -m http.server
```

Windows
```python
$ python -m http.server
```

To access this server, go to the following URL on browser
```
http://localhost:port                 # locally
http://public ipv4 address:port       # from another pc on the same network  
```

To specify a port while creating
```python
$ python3 -m http.server 8080
```
To specify both address and the port
```python
$ python3 -m http.server -b 127.0.0.42 8080
```
To use a ipv6 address
```python
$ python -m http.server -b "::"     # empty ipv6 address
```

**Note:** To find the local IP address

- **macOS:** `ifconfig`
- **Windows:** `ipconfig`
- **Linux:** `ip address` or `hostname -I`

To serve a specific directory
```python
$ python3 -m http.server -d ~/Pictures/
```