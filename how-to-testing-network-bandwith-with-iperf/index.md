# How to Testing Network Bandwith With Iperf


# How to test network speed with iperf

## Install iperf

``` bash
sudo apt-get install iperf3
```

## Testing network speed

### Testing network speed with UDP

* Run command on server
  
  ```bash
  iperf -s -u
  ```
  
* Run command on client
  
  ```bash
  iperf -c -u
  ```
  
* Testing network speed with TCP

	* Server side.

  ``` bash 
  iperf -s
  ```

  * Client side.
  
  ``` bash
  iperf -c
  ``` 
 

## Command for

   ``` bash
  -s  server
  -c client + server IP
  -u udp
  -b bandwith(the max bandwidth
  -t time,how long to send packet.
  -i interval  output per seconds.
  ```

