# Lab 2

## Part 1

### Solving the bug in testReverseInPlace

A failure inducing input: The array `{1, 2, 3}` 

```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```

An input that doesn't induce a failure: The array `{3}`

```
  @Test 
  public void testReverseInPlace2() {
    int[] input1 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
	}
```

The symptom: The input array `{3}` works correctly, returning the array `{3}`. When the tests are initially run without the addition of `testReverseInPlace2`, which contains the failure inducing input, the tests pass.

![Image](noerror.png)

However, the input array `{1, 2, 3}` causes the test `testReverseInPlace2` to fail, since the output differs from the expected output.

![Image](error.png)

The bug: 

Original code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

Code after debugging:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < (arr.length / 2) ; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```

## Part 2
