# PicoCTF2022 - HashingJobApp

## Overview

Points: 100

Category: General

## Description

>If you want to hash with the best, beat this test! nc saturn.picoctf.net 63116


## Hints
1. You can use a commandline tool or web app to hash text.

2. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Approach

1. First I connected to `nc saturn.picoctf.net 63116` on a Linux terminal.

>Please md5 hash the text between quotes, excluding the quotes: 'Backstreet Boys'
>Answer:
>
>340af906f373c781bb56e2e1b51bc325
>
>Correct.
>
>Please md5 hash the text between quotes, excluding the quotes: 'a schoolbus'
>
>Answer: 
>
>dfafe30768c4ded89ca210e239682514
>
>Correct.
>
>Please md5 hash the text between quotes, excluding the quotes: 'angry hornets'
>
>Answer: 
>
>456fdc871d3f9976046da83bcfdd52ff
>
>Correct.
>
>picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}


## Use terminal or any online converter :

`echo -n "sring_to_be_hashed" | md5sum`








