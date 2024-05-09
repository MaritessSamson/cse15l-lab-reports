# Lab Report 3
# Bugs and Commands
---
## Part 1 : Bugs
` static int[ ] reversed (int [ ] arr) `
1. Failure-inducing input for the buggy program
```
@Test
public void testReversedFail(){
  int [ ] input1 = {1,2,3};
  assertArrayEquals(new int[ ] {3,2,1}, ArrayExamples.reversed(input1));
}
```
2.  Non-failing input
```
@Test
public void testReversedPass(){
  int [] input1 = {0,0,0}
  assertArrayEquals(new int[ ] {3,2,1}, ArrayExamples.reversed(input1));
}
```
3.   Systems
    [NEED TO GET SCREENSHOTS OF CODE]
4.   The bug
```
static int [] reversed(int[] arr) {
  int [ ] newArray = new int[arr.length];
  for(int i=0; i<arr.length; i++){
    arr[i] = newArray(arr.length - i - 1);
  }
  return arr;
}
```

```
static int[] reversed (int[] arr){
  int [] newArray = new int[arr.length];
  for(int i=0; i<arr.length; i++){
    newArray[i] = arr(arr.length - i - 1);
  }
  return newArray;
}
```
5. **Why does this fix the issue?**
The bug is found on lines 4 and 5 of the code blocks. The method was supposed to copy elements from `arr` to `newArray`, but instead the elements from `newArray` is copied to `arr`.  `newArray` is instantiated as an array full of zeroes, and so the array returned is `arr` that has been changed to be an array full of zeroes. The fixed code is fixed because it properly copies the elements from `arr` to `newArray` in the reversed order. 
---
## Part 2 : Researching Commands
I chose to research the `less` command. This command allows for the programmer to view a file in a shorter format. Here are a few alternate ways to use `less`.

1. `less -J` - This command scrolls beyond the end of the file. I find this interesting because I am curious what this means for the output. If the computer has already reached the end of the file, what is left to print out to the terminal.
2. `

References:
- [less(1) — Linux manual page](https://man7.org/linux/man-pages/man1/less.1.html)
