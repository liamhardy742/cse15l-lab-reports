# Lab Report 2
Liam Hardy
CSE 15L


# The StringServer `/add-message` path

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



![OneItemAdded](LabReportTwoScreenshots/LabReport2OneStringAdded.png)
When this path is given, the `handleRequest()` method is called. 
The relevant values for this method is of course the `URI url` argument that is passed into the method.
An important part of `url` is if it contains a path, specifically that path being `/add-message` or not, as well as
if the url containts a query, and whether the query's first parameter is "s".
In this case, the path is `/add-message` and the query is `s=Hello%20world!`.
Because of these values, the `finalOutput` String is modified to include a newline character (`\n`) 
and the String that is passed in in the query after the `=`, which is `Hello%20world!`.


![TwoItemsAdded](LabReportTwoScreenshots/LabReport2TwoStringsAdded.png)
