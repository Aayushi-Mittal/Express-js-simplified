# Getting Started with Express.js

## Setting it Up

```
# check the version of node and node package manager(npm)
node --version
npm --version
```

Whenever we create a project using npm, we need to provide a package.json file, which has all the details about our project.

1. Start your terminal/cmd, create a new folder and cd (change directory) into it

```
mkdir project
cd project
```

2. Now to create the package.json file using npm, use the following code. It will ask you for the following information. Just keep pressing enter, and enter your name at the “author name” field.

```
npm init
```

3. Now we have our package.json file set up, we will further install Express. To install Express and add it to our package.json file, use the following command −

```
npm install --save express
# To confirm that Express has installed correctly, run the following command.
ls node_modules
```

4. To make our development process a lot easier, we will install a tool from npm, nodemon. This tool restarts our server as soon as we make a change in any of our files, otherwise we need to restart the server manually after each file modification. To install nodemon, use the following command −

```
npm install -g nodemon
```

## Create an Express Application

Create a new file called index.js and type the following in it.

```
var express = require('express');
var app = express();

app.get('/', function(req, res){
   res.send("Hello world!");
});

app.listen(3000);
```

Save the file, go to your terminal and run the following command.

```
nodemon index.js
```

This will start the server. To test this app, open your browser and go to http://localhost:3000 and a message will be displayed.

<!--
## Routers

We can perform various operations on routes using HTTP methods such as GET, POST, PUT, and DELETE.

The HTTP method is supplied in the request and specifies the operation that the client has requested. The following table lists the most used HTTP methods −

| S. No. | Method | Description |
| ------ | ------ | ----------- |
| 1      | GET    | The GET method requests a representation of the specified resource. Requests using GET should only retrieve data and should have no other effect.                                                       |
| 2      | POST   | The POST method requests that the server accept the data enclosed in the request as a new object/entity of the resource identified by the URI.                                                          |
| 3      | PUT    | The PUT method requests that the server accept the data enclosed in the request as a modification to existing object identified by the URI. If it does not exist then the PUT method should create one. |
| 4      | DELETE | The DELETE method requests that the server delete the specified resource. |


```
const express = require('express');
const app = express();
const router = express.Router();

router.get('/home', (req,res) => {
  res.send('Hello World, This is home router');
});

router.get('/profile', (req,res) => {
  res.send('
    Hello World, This is profile router
  ');
});

router.get('/login', (req,res) => {
  res.send('
    Hello World, This is login router
  ');
});

router.get('/logout', (req,res) => {
  res.send('
   Hello World, This is logout router
  ');
});

app.use('/', router);

app.listen(process.env.port || 3000);

console.log('Web Server is listening at port '+ (process.env.port || 3000));

```

run the code using the following command.

```
node app.js
```

You should see the following message in the terminal.

```
Web Server is listening at port 3000
```
-->

## References
- https://www.tutorialspoint.com/expressjs/expressjs_environment.htm
- https://codeforgeek.com/express-nodejs-tutorial/#express-routers
- https://www.tutorialspoint.com/http/http_methods.htm


## Other Useful Links and Tutorials

### Node.js
- [How To Write and Run Your First Program in Node.js](https://www.digitalocean.com/community/tutorials/how-to-write-and-run-your-first-program-in-node-js)
- [How To Use Node.js Modules with npm and package.json](https://www.digitalocean.com/community/tutorials/how-to-use-node-js-modules-with-npm-and-package-json)
- [How To Create a Web Server in Node.js with the HTTP Module](https://www.digitalocean.com/community/tutorials/how-to-create-a-web-server-in-node-js-with-the-http-module)

### Express.js
- [How To Get Started with Node.js and Express](https://www.digitalocean.com/community/tutorials/nodejs-express-basics)
- [How To Use the req Object in Express](https://www.digitalocean.com/community/tutorials/nodejs-req-object-in-expressjs)
- [How To Use the res Object in Express](https://www.digitalocean.com/community/tutorials/nodejs-res-object-in-expressjs)
- [Official Documentation](https://expressjs.com/en/api.html#express)
- [How To Define Routes and HTTP Request Methods in Express](https://www.digitalocean.com/community/tutorials/nodejs-express-routing)
- [How To Create a Custom Middleware in Express.js](https://www.digitalocean.com/community/tutorials/nodejs-creating-your-own-express-middleware)
- [Database Integration](https://www.tutorialspoint.com/expressjs/expressjs_database.htm)

### Projects
- [Todo application - How To Get Started with the MERN Stack](https://www.digitalocean.com/community/tutorials/getting-started-with-the-mern-stack)
- [How To Build a Lightweight Invoicing App with Node: Database and API](https://www.digitalocean.com/community/tutorials/how-to-build-a-lightweight-invoicing-app-with-node-database-and-api)
