# Lab Report 1

## Part 1

## Part 2

```
 @Test
 public void testReversed() {
   int[] input1 = {1,2,3};
   System.out.print(ArrayExamples.reversed(input1));
   assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
```
![Image](labReport2pic2)
```
@Test
  public void testReversed() {
    int[] input1 = {0};
    System.out.print(ArrayExamples.reversed(input1));
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input1));
  }
```
![Image](labReport2pic1)
