# PicoCTF2019 -mus1c

## Overview

Points: 300

Category: General

## Description 

>I wrote you a song. Put it in the picoCTF{} flag format.


## Hints
1. Do you think you can master rockstar?

## Approach

1. When I opened the file song :
>Put my mind of Pico into This
>my flag is not found
>put This into my flag
>put my flag into Pico
>
>
>shout Pico
>shout Pico
>shout Pico
>
>My song's something
>put Pico into This
>
>Knock This down, down, down
>put This into CTF
>
>shout CTF
>my lyric is nothing
>Put This without my song into my lyric
>Knock my lyric down, down, down
>
>shout my lyric
>
>Put my lyric into This
>Put my song with This into my lyric
>Knock my lyric down
>
>shout my lyric
>
>Build my lyric up, up ,up
>
>shout my lyric
>shout Pico
>shout It
>
>Pico CTF is fun
>security is important
>Fun is fun
>Put security with fun into Pico CTF
>Build Fun up
>shout fun times Pico CTF
>put fun times Pico CTF into my song
>
>build it up
>
>shout it
>shout it
>
>build it up, up
>shout it
>shout Pico

2. I pasted above content in online interpretor of Rockstar programming language and it returned ASCII values :

>114
>
>114
>
>114
>
>111
>
>99
>
>107
>
>110
>
>114
>
>110
>
>48
>
>49
>
>49
>
>51
>
>114


3. I wrote a python script to convert ASCII values into characters :
```
>>> a="""114
... 114
... 114
... 111
... 99
... 107
... 110
... 114
... 110
... 48
... 49
... 49
... 51
... 114"""
>>>for i in a.split():
>>>...     print(chr(int(i)),end="")
rrrocknrn0113r
>>>
```

## Flag :picoCTF{rrrocknrn0113r}








