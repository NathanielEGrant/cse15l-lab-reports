# Lab Report 1

## Part 1

## Part 2

### A failure inducing input
```
 @Test
 public void testReversed() {
   int[] input1 = {1,2,3};
   System.out.print(ArrayExamples.reversed(input1));
   assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
```
![Image](labReport2pic2.png)

### A non-failing input
```
@Test
  public void testReversed() {
    int[] input1 = {0};
    System.out.print(ArrayExamples.reversed(input1));
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input1));
  }
```
![Image](labReport2pic1.png)


### Buggy code
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - 1 -i];
    }
    return arr;
  }
  ```
  
 ### Debugged Code
 ```
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - 1 -i];
    }
    return newArray;
  }
  ```
  In the original code, ```arr``` is being returned even though the function is meant to return a new array. On top of this, the original code was copying the contents of ```newArray``` into ```arr```, which is a problem as ```newArray``` is empty while the copying is being done. So instead of returning a new flipped array, we are essentiall returning an old erased array. So that is why I changed the return statement to return ```newArray``` instead of ```arr```, as well as fixing the variables up in the for loop.
