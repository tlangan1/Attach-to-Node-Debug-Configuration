# Launch versus Attach in VS Code

## A simple example to illustrate the use of launch and attach for debugging

1. Before testing either configuration place a break point in both the function passed to "app.get()" and the function passed to "app.listen()".

1. To run the "launch" version of this example simply run the "launch node app for debugging" debug configuration. As soon as you do so you should hit the break point in the function passed to the app.listen.

1. To run the "attach" version of this example open a terminal window and execute the command "node server.js". Next, run the "attach to running node app for debugging" debug configuration and select the PID of the correct process. Note that if you don't run the "node server.js" command first and you do not have any other node processes running then the list will be empty. Also, note that, unlike in the "launch" version you do not hit the break point in the function passed to "app.listen()". This is because that function was called when the "node server.js" command was executed.

1. In both scenarios, however, if you open a browser to localhost:3000 you should hit the break point in the function passed to "app.get()".
