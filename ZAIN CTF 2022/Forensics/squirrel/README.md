# Challenge name : squirrel

![Badge](https://img.shields.io/badge/CTF-easy-brightgreen) 
![Badge](https://img.shields.io/badge/Date-18%2F03%2F2022-blue)

## Description : 
`an image tells a story, try to discover more details`

:link:[Link](https://hubchallenges.s3.eu-west-1.amazonaws.com/Forensics/squirrel.zip)


## Solution : 

After decompressing the folder , we have an image of a squirrel :

![squirrel](https://user-images.githubusercontent.com/73240347/159070211-9c2ffcc5-dcd3-420a-9a0c-2df5df72195e.jpg)

using strings we got a lot of useless data , but in the middle we found a **mediafire Link** 

![image](https://user-images.githubusercontent.com/73240347/159071223-645facc9-a38e-4f81-a30d-08a31c8297e2.png)

We got another file name iamnotreal.zip , but this time it's protected by password ! . 

So to crack the zip password we use `John The Ripper tool` in Kali Linux .  

`Step`:one: is to create a hash file of our password protected zip file. Using the zip2john utility to generate one.
```console 
kali@kali:~/Desktop$ zip2john iamnotreal.zip > hash.txt
```

`Step`:two: we gonna use the rockyou.txt file wordlist with the following command:
```console 
kali@kali:~/Desktop$ john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
Using default input encoding: UTF-8
Loaded 1 password hash (PKZIP [32/64])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
squirrel07       (iamnotreal.zip/evil/EVIL)
1g 0:00:00:00 DONE (2022-03-18 20:40) 5.000g/s 6328Kp/s 6328Kc/s 6328KC/s srooney981..spalis
Use the "--show" option to display all of the cracked passwords reliably
Session completed
```
After extracting the file , we got a corrupted file , but analyzing his hex we can know that's a jpg file , so let's modify the hex :

Before : 

![image](https://user-images.githubusercontent.com/73240347/159073213-c1bb656c-2c52-4175-8b41-6506a7d324d3.png)


After : 

![image](https://user-images.githubusercontent.com/73240347/159073379-46e099cf-6a37-4fa8-8866-dac386d62345.png)


we got this image : 

![EVIL](https://user-images.githubusercontent.com/73240347/159074325-bdee19e4-7cbf-4510-9403-72df10b30c38.JPG)

Decrypting the given text from base32 to text , we get the flag : 

![image](https://user-images.githubusercontent.com/73240347/159073749-926dbabf-d819-4321-8fe0-e0eaeba734e8.png)

 > # The flag is  {Ev1l_S9uirr3lz}
 



