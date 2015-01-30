# Introduction to node.js
Little tutorial to install and example of use node.js based on the tutorial of the officia page(see fonts section)

##Introduction
Node.js is an open source, cross-platform runtime environment for server-side and networking
applications. Node.js applications are written in JavaScript, and can be run within the Node.js 
runtime on OS X, Microsoft Windows, Linux, FreeBSD, and IBM i.

Node.js provides an event-driven architecture and a non-blocking I/O API that optimizes an 
application's throughput and scalability. These technologies are commonly used for real-time 
web applications.

Node.js uses the Google V8 JavaScript engine to execute code, and a large percentage of the basic 
modules are written in JavaScript. Node.js contains a built-in library to allow applications to 
act as a Web server without software such as Apache HTTP Server or IIS

##Fonts
* Font http://es.wikipedia.org/wiki/Node.js (introduction)
* Font http://nodejs.org/ (examples)
* Font Manual node in command man. (develop tutorial)

##Instalation
1-First run  http://nodejs.org/  
2-Push install:  
imagen install  
3-When the file is downloaded open shell and put the following commands:  
  To decompress:  
      `$ tar xzvf node-v0.10.36.tar.gz`  
  To install:  
      `$ cd node-v0.10.36`  
      `$ sudo make`
      `$ sudo make install`  
      `$ sudo ./configure`  
  Delete temporary stuff:  
      `$ cd ..` 
      `$ rm -rf node-v0.10.36.tar.gz node-v0.10.36`  
We have now installed node.js

##Ejamples of use
This simple web server written in Node responds with "Hello World" for every request.  
```
var http = require('http');  
http.createServer(function (req, res) {  
  res.writeHead(200, {'Content-Type': 'text/plain'});  
  res.end('Hello World\n');  
}).listen(1337, '127.0.0.1');  
console.log('Server running at http://127.0.0.1:1337/');  
```
To run the server, put the code into a file example.js and execute it with the node program from the command line:  

`$ node example.js`  
Server running at http://127.0.0.1:1337/  


Here is an example of a simple TCP server which listens on port 1337 and echoes whatever you send it:  
`$ node`

And write:  

```
>var net = require('net');

>var server = net.createServer(function (socket) {
  socket.write('Echo server\r\n');
  socket.pipe(socket);
});

>server.listen(1337, '127.0.0.1');
```  
you can change server configuration inline with command node. This produces a  
loop where the code are written and executed in real time.

