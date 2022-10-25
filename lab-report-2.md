# Lab Report 2
## Part 1
**Code for Simplest Search Engine**
```
import java.net.URI;
import java.io.IOException;
import java.util.*;

class Handler implements URLHandler {
    ArrayList<String> stringList = new ArrayList<String>();

    public String handleRequest(URI url) {
        System.out.println("Path: " + url.getPath());
        if(url.getPath().equals("/")){
            return String.format("Current list of Strings: " + stringList.toString());
        }
        if (url.getPath().equals("/add")) {
            String[] parameters = url.getQuery().split("=");
            stringList.add(parameters[1]);
            return String.format("You added " + parameters[1] + " to the list! The full list of strings is " +stringList.toString());
        }
        if (url.getPath().equals("/search")){
            String[] parameters = url.getQuery().split("=");
            String printList = "";
            for(int i = 0; i < stringList.size(); i++){
                if(stringList.get(i).contains(parameters[1])){
                    printList += stringList.get(i) + " ";
                }
            }
            if(printList.length() == 0){
                return String.format("This phrase does not exist in the search engine.");
            }else{
                return String.format("Here are the results of your search: " + printList);
            }
        }
        return "404 not found!";
    }
}
public class SearchEngine{
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
**Usages:**
1. ![Image] (https://raw.githubusercontent.com/caz002/cse15l-lab-reports/main/Screen%20Shot%202022-10-25%20at%203.10.49%20PM.png)
The method handleRequest is called. The argument passed is the url: localhost:4000/add?=peach. The field variable is an array of strings called parameters, which consists of the results of the query of the url after it is passed through the split method. The element at index 1 is the string being added to and stored inside the webpage using the array list stringList. Neither the url or the array list parameters change over the course of the process.
2. ![Image] (https://raw.githubusercontent.com/caz002/cse15l-lab-reports/main/usage2.png)
The method handleRequest is called. The argument passed is the url: localhost:4000/add?=pencil. The field variable is an array of strings called parameters, which is the array produced by calling the method split(“=”) on the query of the url. parameters[1] contains the string being stored inside the website’s server. The website keeps track of stored elements in an arraylist called stringList. The argument or field variables do not change over the course of this process.
3. ![Image]
The method handleRequest is called. The argument passed is the url: localhost:4000/search?=pea. The field variables are the string arraylist parameters and the string printlist. Parameters takes the values of the query in the url after it is passed through the split method. The element at index 1 of parameters stands for the string that is being searched for throughout the stored strings in stringList. The code iterates through the stored strings on the webpage in the array list stringList, checking to see if each element contains the search phrase, and if it does, adding it to printlist. The final line of the method prints the values of printlist onto the webpage. Throughout the code, the url and parameters does not change, but printlist does.

##Part 2
###Bug One
- Failure-Inducing Input:
- Symptom:
- Bug:(from ListExample.java)
###Bug Two
- Failure-Inducing Input:
- Symptom:
- Bug:(from LinkedListExample.java)
