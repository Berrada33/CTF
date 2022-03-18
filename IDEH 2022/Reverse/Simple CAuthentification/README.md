# Challenge name : Simple CAuthentification

![Badge](https://img.shields.io/badge/CTF-easy-brightgreen)

## Description : 
*Author: ***m4rc0s**** 


You should reverse this binary to know the flag.

Attempt to get the password

[Download Attachment](https://s3.eu-west-3.amazonaws.com/crisis-assets/crisis_attachements/KCEPBe2Emug0PeTspqA2gcEEOW0UeCn0BxnCT8MS.zip)


## Solution : 

After  extracting the compressed folder , we get an executable file 

![image](https://user-images.githubusercontent.com/73240347/159056306-7bcc5727-a058-4bee-bf40-7c9ab0cd2092.png)

So in order to run it , *First* we have to change **permission** with the command *chmod +x auth* then ./auth 

![image](https://user-images.githubusercontent.com/73240347/159056737-314750a0-1e7b-4822-bac5-79cdb4a9009c.png)

we need a password to pursuit ! But if we do **strings auth** we get a lot of data to analyse including this password  

![image](https://user-images.githubusercontent.com/73240347/159057160-544ea52e-650b-4f88-bb9a-151b394fa8c7.png) 

Although is mentioned incorrect password , if we enter it in the binary file we get our flag : 

![image](https://user-images.githubusercontent.com/73240347/159057547-e9e84eaa-1b95-482d-91e1-cdea7afac539.png)



