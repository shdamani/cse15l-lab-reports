# LAB REPORT 2 - SHLOK DAMANI A17373189
## In the following I will
- Write a web server called StringServer
- Analyze a bug from the week 3 lab session and fix it
- What I learned in the last 2 weeks :)
# 1) Web server
,,,
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String s="";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(s);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")){
                for(int i=1;i<parameters.length;i++){
                   s=s+parameters[i];
                }
                String s1=s;
                s=s+"\n";
                return String.format(s1);
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
,,,
