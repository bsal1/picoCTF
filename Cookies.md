# PicoCTF2021-Cookies

## Overview

Points: 40

Category: Web Exploitation

## Description

>Who doesn't love cookies? Try to figure out the best one. http://mercury.picoctf.net:27177/


## Hints
No Hints available.

## Approach 

1. Go to http://mercury.picoctf.net:47967/


2. Open Developer tool using F12 key. 

3. Storge -- Cookies

4. Select picoCTF site cookie and double click on values.

5. Try changing the value and refresh the tab to get new result.

6. Each value has different result.

7. Try changing the values manually and you will get the flag.

8. Alternatively , we can use burp intruder to bruteforce the values and make our task easy.

9. Intercept the result in burp.
```sh
GET /check HTTP/1.1
Host: mercury.picoctf.net:27177
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.5304.107 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Referer: http://mercury.picoctf.net:27177/
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Cookie: name=-1
Connection: close
```

10. Send to intruder and turn off intercept.

11.  Attack type : Sniper 

12. Move to payloads subtab.
  
  >Payload type : Numbers
  >
  >From : 1
  >
  >To : 30
  >
  >Step:1

13. Start atatck.

14. Click on each payload and check response below. 

15. Render the request for easiness.

16. Check for flag.

## FLAG : picoCTF{3v3ry1_l0v3s_c00k135_064663be}
