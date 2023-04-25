**Lab 2**

**Part 1:**
String Server Code:
  ![Image](stringservercode.png)
  

  ![Image](sstest1.png)
  ![Image](sstest2.png)
  
**Part 2:**
  
  Failed JUnit Test:
  ![Image](junitbug.png)
  
  Passed JUnit Test:
  ![Image](junitpass.png)
  
  Code Before Fix:
  ```
  static void reverseInPlace(int[] arr) {
      for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
      }
    }
  ```
  
  Code After Fix:
  ```
  static void reverseInPlace(int[] arr) {
      for(int i = 0; i < arr.length/2; i += 1) {
        int temp = arr[i];
        arr[i] = arr[arr.length - i - 1];
        arr[arr.length - i - 1] = temp;
      }
    }
   ```
  
**Part 3:**
  During week 2 in lab I learned how to create a web server that could be altered depending on what was written in the URL. By the end of the lab session I   had implemented a counter that counted when an add command was entered in the URL and also have my server appear on someone else's computer.