# Lab Report 3 - Bugs and Commands (Week 5)
## Part 1 

**A Failure-Inducing Input**

`	
@Test 
	public void Fail_testReverseInPlace() {
    int[] input1 = { 3, 4, 5, 6, 7 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 7, 6, 5, 4, 3 }, input1);
	}
 `
![Image](failure-inducing_input.png)

The function I am testing is:
`  
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
`

 **An Input That Doesn’t Induce a Failure**

 `
 @Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
 `

![Image](success_input.png)

The function I am testing is:
`  
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
`
