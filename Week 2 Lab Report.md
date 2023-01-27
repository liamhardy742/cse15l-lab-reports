# Lab Report 2
Liam Hardy
CSE 15L


# The StringServer `/add-message` path
## Part 1
**Code for my implementation of the server and URL handler**
```
class Handler implements URLHandler {
   
    String finalOutput = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return finalOutput;
        } 
        else {
            if (url.getPath().contains("/add-message")) {
                    String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    for (int i = 1; i < parameters.length; i++) {
                        finalOutput = finalOutput + parameters[i] + "\n";
                    }
                    return finalOutput;
                }
            }
            return "404 Not Found!";
        }
    }
}

public class VerticalStringList {
    public static void main(String[] args) throws IOException {
       
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler()); 
    }
}
```
  
  
  
  
**Server after one String has been added**
![OneItemAdded](LabReportTwoScreenshots/LabReport2OneStringAdded.png)
When this path is given, the `handleRequest()` method is called. 
The relevant value for this method is of course the `URI url` argument that is passed into the method.
An important part of `url` is if it contains a path, specifically that path being `/add-message` or not, as well as
if the url containts a query, and whether the query's first parameter is "s".
In this case, the path is `/add-message` and the query is `s=Hello%20world!`, which is equivalent to `s=Hello world!`.
Because of these values, the `finalOutput` String is modified to include a newline character (`\n`) 
and the String that is passed in in the query after the `=`, which is `Hello world!`. The value of `finalOutput` changed
from `""` to `"Hello world!\n"`.
  
  
  
  

**Server after two Strings have been added**
![TwoItemsAdded](LabReportTwoScreenshots/LabReport2TwoStringsAdded.png)
This path is the same path as the previous screenshot, so the `handleRequest()` method is called.
The `URI url` argument is once again the relevant value for this method, and in this case, the path is still `add-message` and
the query is now `s=Oh%20hi%20there!`, equivalent to `s=Oh hi there!`.
Because of these values, the `finalOutput` String goes from being `"Hello world!\n"` to being `"Hello world!\nOh hi there!"`.
## Part 2
  
The bug that I am choosing from lab 3 lies in the `reversed(int[] array)` method in the `ArrayExample.java` file. Which is shown below. 
```
// This is the method being tested.
// Returns a *new* array with all the elements of the input array in reversed
// order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
A failure inducing input is shown in the tester below,
```
@Test
  public void testReversed() {
    int[] input1 = {1,2,3,4,5};
    int[] output1 = {5,4,3,2,1};
    int[] result = ArrayExamples.reversed(input1);
    printOutput(result);
    assertArrayEquals(output1, ArrayExamples.reversed(input1));
  }
```
This input does not induce failure:
```
@Test
  public void testReversedEmpty() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
