# key-Value-Database
It a implementation of key-value database using python that perform create , read and delete operations 

Problem: Build a file based key-value data store that support 
->create 
->read 
->delete

operations , the data stored must be locally stored in the system .

The database is stored locally in json format I have taken 2 databases, one is master database and the other is temporary database 
temporary data will store all the operations for one single process .

I have taken key as a string and pair as a number , we can also modify the code so that pair becomes a string,number,list,dict...or any data structure that is supported in the dictionary . I have also included timeout concept 

Also ,I have implemented all the code in same notebook , if we want to make a library then we have to create 2 .ipynb notebook one with all the functions and another one will contain all the instances and calling of these functions

![](video.gif)




The data store will support the following :

It can be initialized using an optional file path. If one is not provided, it will reliably create itself in a reasonable location on the laptop.
A new key-value pair can be added to the data store using the Create operation. The key is always a string - capped at 32chars. The value is always a JSON object - capped at 16KB.
If Create is invoked for an existing key, an appropriate error must be returned.
A Read operation on a key can be performed by providing the key, and receiving the value in response, as a JSON object.
A Delete operation can be performed by providing the key.
Every key supports setting a Time-To-Live property when it is created. This property is optional. If provided, it will be evaluated as an integer defining the number of seconds the key must be retained in the data store. Once the Time-To-Live for a key has expired, the key will no longer be available for Read or Delete operations.
Appropriate error responses must always be returned to a client if it uses the data store in unexpected ways or breaches any limits
The file size never exceeds 1GB
