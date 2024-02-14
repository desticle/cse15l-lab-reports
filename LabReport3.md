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
