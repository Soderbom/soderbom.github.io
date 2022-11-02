---
layout: post
title: Hidden functions
date: 2022-11-01 19:00:00 +200
categories: [beginner, ctf, reversing]
tag: [beginner, ctf, reversing, gdb]
---

It is quite common for beginner CTFs, that includes a binary, to hide some information in a function that is supposed to be unreachable or use a function to obfuscate a flag. Today we are finding out how to bypass all that nonsense. 

## The code
Here we have some simple C code. The function *no_way_here* is our goal, but it is never called.

``` c
#include <stdio.h>

void no_way_here() {
	printf("Oh, I was wrong. You found it!");
}

int main() {
	printf("You haven't got it yet\n");
	return 0;
}
```

Compile the code with the command below and let's go!
``` bash
gcc demo.c -o demo
```

## GDB
To gain access to the hidden function we can use GDB. Start it with:
``` bash
gdb ./demo
```

If you just run the program you get the expected "You haven't gotten it yet" line. 


OPTIONAL: If you already know which function you want to run you can skip this step. If you don't know the function name you can use the command below to list all functions.
``` bash
info functions
```
![](/assets/images/2022-11-02/gdb_info_functions.png)

Aha, there it is! Let's set a break point at main so we don't immediatly exit the program when we run it.
``` bash
b main
run
```

Now, let's jump to our function with the following command:
``` bash
jump no_way_here
```

![](/assets/images/2022-11-02/jump_result.png)
And there it is! The output of our hidden function.

## Try it out!
If you are just getting started I can recommend to test your skills in the following TryHackMe room. The difficulty is ranging from *just run the file* to actually getting some use out of this post towards the end. <br>
[https://tryhackme.com/room/reverselfiles](https://tryhackme.com/room/reverselfiles)

If you want to dig deep I can recommend Practical Binary Analysis by Dennis Andriesse. The book will teach you a lot about binaries and how they work AND is accompanied with a VM full of challenges!<br>
[https://practicalbinaryanalysis.com/](https://practicalbinaryanalysis.com/)