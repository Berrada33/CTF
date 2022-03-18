# Challenge name : Simple CAuthentification

![Badge](https://img.shields.io/badge/CTF-easy-brightgreen)

## Description : 
*Author: ***sicmundos**** 

Some weird number keeps calling me, can you extract it?

Dont forget to wrap what you have found inside CRISIS{}

[Download Attachment](https://s3.eu-west-3.amazonaws.com/crisis-assets/crisis_attachements/FEb0joyUynFtqOH4XDdDMqr03FIoxVFQrr7ecdCB.zip)



## Solution : 

After extracting files from the compressed folder , we have a *.wav* file , after playing it we hear like entering numbers in phone : it's the **DTMF** 

In order to get the numbers , we just have to use online decoders like this : https://unframework.github.io/dtmf-detect/#/ and upload our file : 

![image](https://user-images.githubusercontent.com/73240347/159061488-040b57dd-83e9-4ef8-855e-cac262a5fea2.png)

The `flag` are the numbers , no need to decode them , as mentioned in the description 

