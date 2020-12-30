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

```python
#Wanted to show that we can use what ever we want to store in key-value data store
#In Code that i have implemented ,string key and int value is what i have used
dict={}
dict["name"]="sumit"                                #value is string 
dict["age"]=16                                      #value is int
dict["Subject"]=["Python","C++"]                    #value is List
dict["random"]=["abc",1,["2",3]]                    #value is list within list
dict["inside_dict"]={1:2}                           #value is dictionary
print(dict)

Output: {'name': 'sumit',
 'age': 16,
 'Subject': ['Python', 'C++'],
 'random': ['abc', 1, ['2', 3]],
 'inside_dict': {1: 2}}

```


Also ,I have implemented all the code in same notebook , if we want to make a library then we have to create 2 .ipynb notebook one with all the functions and another one will contain all the instances and calling of these functions

```python
#For example : Make 2 .ipynb notebook , save it in one directory A.ipynb and B.ipynb
#If we want to use A.ipynb as library for B.ipynb
#we can import A file as Library in B using this simple one line code
%run A.ipynb
```

![](video.gif)


Reference :
https://en.wikipedia.org/wiki/Key%E2%80%93value_database

https://www.w3schools.com/js/js_json_objects.asp

https://en.wikipedia.org/wiki/Thread_safety


