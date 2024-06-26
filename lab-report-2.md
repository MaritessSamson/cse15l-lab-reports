# Lab Report 2
## Servers and SSH Keys
### Part One
---
**My code for ChatServer**
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // Where the chat log, the current user, and message will be saved
    String chatLog = "";
    String user = "";
    String message = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            if (chatLog.equals("")){
                return "No chat found";
            }
        }
        else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")){
                String[] firstHalfParam = parameters[1].split("&");
                message = firstHalfParam[0];
                if (firstHalfParam[1].equals("user")){
                    if (parameters.length == 3) user = parameters[2];
                    chatLog += String.format("%s: %s", user, message) + "\n";
                    System.out.println(chatLog);
                    return chatLog;
                }
            }
        }
        return "404 Not Found!";
    }
}
class ChatServer {
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
**First example of using /add-message**
![Image](lab-report-2-part1.1.png) 
This screenshot demonstrates the portion of the code using /add-message successfully. It passes through all of the `if` statements which then separates all of the arguments and saves the messages and users to a chat log. To the methods, the relevant arguments are in the strings, "everything's fine bruh", and "someGuy". The first string is assigned to the `message` variable and the second string is assigned to the `user` variable.  The variables change in order to make the full message and add it to the `chat log` variable.

**Second example of using /add-message**
![Image](lab-report-2-part1.2.png)
This screenshot also demonstrates the portion of the code using /add-message successfully. It passes through all of the `if` statements which then separates all of the arguments and saves the messages and users to a chat log. To the methods, the relevant arguments are in the strings, "hi, im watching Dune right now", and "ME!Maritess:)". The first string is assigned to the `message` variable and the second string is assigned to the `user` variable.  The variables change in order to make the full message and add it to the `chat log` variable.
### Part Two
---
1. ![Image](lab-report-2-part2.1.png)
2.  ![Image](lab-report-2-part2.2.png)
3.  ![Image](lab-report-2-part2.3.png)

### Part Three
---
All of week two and three are completely new content to me, but to be specific, I learned more about the 'ssh' command and connecting to remote servers. The `ssh` command allows for the programmer to operate from a different location on another server.
