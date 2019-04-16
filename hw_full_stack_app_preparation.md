# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?

The file create_router.js is responsible for creating the routes with the requests.

2. What are the the responsibilities of server.js?

Server.js sets up the path to the static files and allows the client to connect to the server and the database. Once it is set up, it listens.

3. What are the responsibilities of the `gamesRouter`?

'gamesRouter' is the router which is instanced out of the gamesCollection when a new collection called 'games' is created. Games router is the router which sets up the route paths.

4. What process does the the client (front-end) use to communicate with the server?

The client uses express to communicate with the server.

5. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

It takes a request and response.

6. Which of the games API routes does the front-end application consume (i.e. make requests to)?

index, create, delete

7. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

MongoDB driver allows us to access and interact with the MongoDB database.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

ObjectId is a constructor which creates a new ObjectID instance. This objectID is provided so each document in the database has a unique identifier.
