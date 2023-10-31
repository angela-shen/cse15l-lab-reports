# Lab 2

## Part 1

`StringServer.java` code:
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> words = new ArrayList<String>();
    int num = 0;
    String list = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return list;
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
		            num++;
                    words.add(parameters[1]);
                    list += String.format("%d. %s\n", num, parameters[1]);
		            return list;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
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

StringServer:

![Image](ss1.png)

![Image](ss2.png)

## Part 2

File containing SSH key: 
![Image](path.png)

Path to private key:

![Image](rsa1.png)

Path to public key:

![Image](rsa2.png)

`ssh` in `ieng6`:

![Image](ssh1.png)

## Part 3

In lab, I learned that an SSH key can be used to ssh into a remote server without a password. I also learned that SCP can be used to copy files between remote and local servers.

