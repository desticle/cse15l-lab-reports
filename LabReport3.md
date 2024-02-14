**Lab Report 3**
---
***Part 1***

**The Bug**
The `reverseInPlace` method does not return a reversed array. Instead, it mirrors the second half of the array backwards onto the first half. Thus, it creates a symmetrical array.

**Failure-Inducing Input**
```
@Test 
	public void failureTestReverseInPlace() {
    int[] input1 = {0, 1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5, 4, 3, 2, 1, 0}, input1);
	}
```

**Non-Failure-Inducing Output**
```
@Test 
	public void noFailureTestReverseInPlace() {
    int[] input1 = {0, 1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5, 4, 3, 3, 4, 5}, input1);
	}
```

**Symptom**
![Image](ss5.png)

**Fix**

*Before*
```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

*After*
```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    int tempArray[] = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      tempArray[i] = arr[arr.length - i - 1];
    }
    for(int i = 0; i < arr.length; i++){
      arr[i] = tempArray[i];
    }
  }
```

**Explanation**
The original code would start at the beginning of the array, and change the beginning values (moving forward) to the last values (moving backward). This meant that when it was time for the last values to be changed to the beginning values, the beginning values had already been changed. 

I created a temporary new array with the length of the original array and to hold the reversed values so that the first changes would not interfere with the last. I then transferred all of the temporary reversed values to the original array.

***Part 2***
