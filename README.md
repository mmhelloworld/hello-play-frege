#A simple Play application with Frege#
This is a simple play application written in Frege to demonstrate how we can use Frege with Play.

Since Play supports Java, it is actually very easy to use the Java API from Frege 
even though we don't have native Play support for Frege yet. 
The application is basically JSON-in and JSON-out. 
A Frege program reads a parameter from a JSON POST request and responds with a JSON response that greets the user.

##How to run##
1. Run `activator run` to compile and start the server.
1. Then send a JSON post request.
   For example, with `curl`:
   
   ```
   $ curl --header "Content-type: application/json" --request POST --data '{"name": "Play Frege"}' http://localhost:9000/greet
   
   {"message" : "Hello, Play Frege"}
   
   ```
   