# How to Enable Http Api Service Locally


**How to enable API serivce on VyOS**

## How to enable API serivce on VyOS

After these days, I wrote some vyos shell script to auto detect network status and automatacally change some settings. In the way There will be new configuration to loading directly and hold the configuration mode for a longer time. This is not in a smart way.

Another better option, What if we can change settings of vyos with api?

## enable api http service localy
### Enable apt service with socket mode 
```bash
set service https api socket 
```

### Test settings

```bash
curl --unix-socket /run/api.sock -X POST -Fkey=qwerty -Fdata='{"op": "showConfig", "path": []}' http://localhost/retrieve
```





