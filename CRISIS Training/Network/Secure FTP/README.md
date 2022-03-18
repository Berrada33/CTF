# Challenge name : Secure FTP 



## Description : 
*Author: ***m4rc0s**** 

I did some file upload on my server using FTP the most secure protocol. I guess no one will know that my username access is critical. 

[Download Attachment](https://s3.eu-west-3.amazonaws.com/crisis-assets/crisis_attachements/sLO6ycs3WLUPgEQPsXiiPltVFwuLt60pTNuYgh7j.zip)


## Solution :one:: 

After downloading the compressed folder and extracting it , we see that's contains a file named t1_2022.pcapng 

![image](https://user-images.githubusercontent.com/73240347/159010754-6ce4968b-9326-442c-9087-d30d58101d41.png)

According to the category , title of challenge and description , it's clear that we gonna use a network protocol analyzer like **Wireshark** or **NetworkMiner** .

Using Wireshark , opening the file , we see a lot of captured packets 

![image](https://user-images.githubusercontent.com/73240347/159011653-9af84ddf-d020-4fc8-a81c-94652bfdf492.png)

We have just to search for ftp , as mentioned in the title , and now we get 7 packets to analyse , the flag is shown in plain text 

![image](https://user-images.githubusercontent.com/73240347/159012191-efa3388c-f791-4539-bc13-f4b196997a1c.png)

In general case , we have to follow **TCP STREAM** and search for the flag manually if it's not shown at first place . 

![image](https://user-images.githubusercontent.com/73240347/159012405-e487a743-e1bf-4191-9a94-21d8f1c24cd6.png)

## Solution :two:: 

There is another solution for this kind of challenge , is **always try to open the file with linux and do grep first** , it takes less than 30 seconds and very useful :  

![image](https://user-images.githubusercontent.com/73240347/159016608-650c3bc5-4287-42ea-af71-ceed39dcb28b.png)





