# Nice netcat


# Overview

>Points: 15
>
>Category: General



# Description

 >There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net 43239, but it doesn't speak English...


# Hints

>1. You can practice using netcat with this picoGym problem: what's a netcat?
>2. You can practice reading and writing ASCII with this picoGym problem: Let's Warm Up



# Approach

1. First I connected to mercury.picoctf.net 22902 on a Linux terminal.
      
2. It returned ascii values in string (not int) then I did this to get flag:
 ```sh
      nc mercury.picoctf.net 22902 >> a.txt
      python3
      >>f=open("a.txt")
      >>for i in f :
      ... print(chr(int(i)),end="")
  ```  
      
 # Flag : picoCTF{g00d_k1tty!_n1c3_k1tty!_d3dfd6df}
    
