# Lab Report 2 - Servers and SSH Keys (Week 3)
## Part 1 

**The code for my `StringServer`**
---
![Image](CodeForStringServer.png)

**Using `/add-message?s=Hello`**
---
![Image](1Using'Hello'.png)

I called `getPath()`, `equals()`, `contains(String)`, `getQuery()` and `split(String)`. I use `getPath().contains("/add-message")` to see if url the path contain "/add-message". Next I use `getQuery().split("=")` to split the query(everthing after `?`) into a string array that has two elements. The index 0 is the string before `=`, the index 1 is the string after `=`. So in this specific request `/add-message?s=Hello`, `parameter[0]` would be `s` and `parameter[1]` would be `Hello`. Integer variable `num` is to keep track the amount of the total string list. And after this specific request `/add-message?s=Hello`, num will plus one(after this request, num became 1) and the string `Hello` will be added into the string list since the `parameter[0]`(in here, the string after `?` and before `=`) is `s`.

**Using `/add-message?s=How are you`**
---
![Image](2Using'How_are_you'.png)

I called `getPath()`, `equals()`, `contains(String)`, `getQuery()` and `split(String)`. I use `getPath().contains("/add-message?s=How are you")` to see if the url path contain "/add-message". Next I use `getQuery().split("=")` to split the query(everthing after `?`) into a string array that has two elements. The index 0 is the string before `=`, the index 1 is the string after `=`. So in this specific request `/add-message?s=How are you`, `parameter[0]` would be `s` and `parameter[1]` would be `How are you`. Integer variable `num` is to keep track the amount of the total string list. And after this specific request `/add-message?s=How are you`, num will plus one(after this request, num became 2) and the string `How are you` will be added into the string list since the `parameter[0]`(in here, the string after `?` and before `=`) is `s`. We also notice that the space became `+`. Becuase on EdStem, the space on URL is being process as `%20`.


## Part 2

**The path to the private key for your SSH key for logging into ieng6**
---
![Image](3PrivateKey.png)

**The path to the public key for your SSH key for logging into ieng6**
---
![Image](4PublicKey.png)

**Log into ieng6 without being asked for a password.**
---
![Image](5LoginWithoutPassword.png)

## Part 3
I have learned ssh to a remote server and how to run the server either on EdStem or on ieng6, and interact with it by using the "path" and "query" I've also leared how to run the server on my local computer, and lastly using SSH key to connect to ieng6 server without being asked for a password.
