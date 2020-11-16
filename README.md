# HTTP-BigIP-Cookie-NG
Decodes any unencrypted F5 BIG-IP cookies in the HTTP response. In contrast to the nmap nse script `http-bigip-cookie` (https://nmap.org/nsedoc/scripts/http-bigip-cookie.html), this extension does not only support the default ipv4 pool member but rather ipv4 pool memebers in non-defaul route domains as well. See here for more info: https://support.f5.com/csp/article/K6917

```
$ nmap -p 443 --script=./http-bigip-cookie-ng.nse 127.0.0.1
Starting Nmap 7.91 ( https://nmap.org )
Nmap scan report for 127.0.0.1
Host is up (0.084s latency).

PORT    STATE SERVICE
443/tcp open  https
| http-bigip-cookie-ng:
|   BIGipServer~Test-HTTPS:
|     address:
|       type: ipv4 non-default route domain
|       host: 192.168.253.69
|_    port: 443

Nmap done: 1 IP address (1 host up) scanned in 0.81 seconds
```