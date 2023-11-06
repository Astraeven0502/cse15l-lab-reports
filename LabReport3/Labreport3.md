# Lab Report 3 - Bugs and Commands (Week 5)
## Part 1 - Bugg for `testReverseInPlace`

**A Failure-Inducing Input**
---
```	
@Test 
public void Fail_testReverseInPlace() {
  int[] input1 = { 3, 4, 5, 6, 7 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 7, 6, 5, 4, 3 }, input1);
}
```
![Image](failure-inducing_input.png)

The function I am testing is:
```  
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

 **An Input That Doesn’t Induce a Failure**
---
```
@Test 
public void testReverseInPlace() {
  int[] input1 = { 3 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 3 }, input1);
}
```

![Image](success_input.png)

The function I am testing is:
```  
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

**The Symptom**
---
![Image](symptom.png)

Here is the test I used:
```
@Test 
public void Symptom1_testReverseInPlace() {
  int[] input1 = { 1, 4, 7, 9, 14, 19, 23 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 23, 19, 14, 9, 7, 4, 1 }, input1);
}
@Test 
public void Symptom2_testReverseInPlace() {
  int[] input1 = { 3, 4, 5, 6, 7 }; 
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 7, 6, 5, 4, 3 }, input1);
}
```

**The Bug**
---
Before fixed:
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

After fixed: 
```
static void reverseInPlace(int[] arr) {
  int[] tempArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    tempArray[i] = arr[arr.length - i - 1];
  }
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = tempArray[i];
  }
}
```

I create another array that store the value then assign the reversed value back. Because before the fix, the same array are being use to store elements, the first element lost when the first `FOR` loop is excuted.


## Part 2 - `find` Command

**-name**
---
**On Files**

Command:
```
find -name preface.txt
```
Output:
```
./911report/preface.txt
```

**On Directories**

Command: 
```
find -name 911report
```
Output: 
```
./911report
```

Found from: https://www.redhat.com/sysadmin/linux-find-command

**-iname**
---
**On Files**

Command: 
```
find -iname "chapter*.txt"
```
Output: 
```
./911report/chapter-1.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
./911report/chapter-12.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-2.txt
./911report/chapter-3.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-8.txt
./911report/chapter-9.txt
```

**On Directories**

Command: 
```
find -iname "bio*"
```
Output: 
```
./biomed
```

Found from: https://www.redhat.com/sysadmin/linux-find-command

**-size**
---
**On Files**
Command: 
```
find ./plos/pmed.0020191.txt -size 1k
```
Output: 
```
./plos/pmed.0020191.txt
```

**On Directories**

Command: 
```
find ./911report -size +1k
```
Output: 
```
./911report
./911report/chapter-1.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
./911report/chapter-12.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-2.txt
./911report/chapter-3.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-8.txt
./911report/chapter-9.txt
./911report/preface.txt
```

Found from: https://tecadmin.net/linux-find-command-with-examples/

**-type d**
---
**On Files**

Command:
```
find ./911report/chapter-1.txt -type d
```
Output:
```
/* Print nothing */
```

**On Directories**

Command: 
```
find ./ -type d
```
Output: 
```
./
./911report
./biomed
./government
./government/About_LSC
./government/Alcohol_Problems
./government/Env_Prot_Agen
./government/Gen_Account_Office
./government/Media
./government/Post_Rate_Comm
./plos
```

Found from: https://www.tecmint.com/35-practical-examples-of-linux-find-command/
