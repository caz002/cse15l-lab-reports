![Image of Desktop] (<img width="618" alt="Screen Shot 2022-10-06 at 3 36 30 PM" src="https://user-images.githubusercontent.com/115192246/194431227-a06c2777-b77a-4f19-bdc8-408ac6ade38b.png">)




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
