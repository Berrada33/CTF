# Challenge name : Simple CAuthentification

![Badge](https://img.shields.io/badge/CTF-easy-brightgreen)

## Description : 
*Author: ***m4rc0s**** 


You should reverse this binary to know the flag.

Attempt to get the password

[Download Attachment](https://s3.eu-west-3.amazonaws.com/crisis-assets/crisis_attachements/KCEPBe2Emug0PeTspqA2gcEEOW0UeCn0BxnCT8MS.zip)


## Solution : 

After  extracting the compressed folder , we get an executable file 

```console
Ubuntu@Ubuntu:~/Downloads/KCEPBe2Emug0PeTspqA2gcEEOW0UeCn0BxnCT8MS$ file auth
auth: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=5f8fefb60a5f9db2b9b492e534c43a0e01f443da, for GNU/Linux 3.2.0, not stripped
```

So in order to run it , *First* we have to change **permission** with the command *chmod +x auth* then ./auth 
```console
Ubuntu@Ubuntu:~/Downloads/KCEPBe2Emug0PeTspqA2gcEEOW0UeCn0BxnCT8MS$ chmod +x auth && ./auth
Please insert your password : 
flag
Incorrect Password
```
we need a password to pursuit ! But if we do **strings auth** we get a lot of data to analyse including this password  

![image](https://user-images.githubusercontent.com/73240347/159057160-544ea52e-650b-4f88-bb9a-151b394fa8c7.png) 

Although is mentioned incorrect password , if we enter it in the binary file we get our flag : 
```console
Ubuntu@Ubuntu:~/Downloads/KCEPBe2Emug0PeTspqA2gcEEOW0UeCn0BxnCT8MS$ ./auth
Please insert your password : 
DfX2NNNNN==
CRISIS{c8xo1bD}
```



