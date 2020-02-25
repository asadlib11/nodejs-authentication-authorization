This is a node js server which shows the implementation of user authentication and authorization. 
I will be using JSON web token (JWT) for authentication and authorization.

Following are the actions:
    Define the environment variables.
    Create an express server.
    Connect to the database.
    Create the User Model.
    Create the necessary routes.
    Create the auth middleware and more routes.

Packages to install:
    mongodb, mongoose, bcryptjs, validator, jsonwebtoken
    nodemon as dev dependancy
    
Usage:
    npm install #to install all dependencies
    npm start  #to run the project on your machine

Project flow details:
    You can signup a user, then it gets logged in and a token is added to the database for that specific user. If you login from another device again a token will be provided that will be used by front-end or any other service that will be using our server, in order to authenticate or authorize the user.
    For logging out, there are two funtionalities, log out from current device or logout from all devices.
    Log out from current device will only remove current token from database and you can no longer pass authentication from that device.
    Log out all rest api will remove all the tokens from database for the logged in user and user cannot pass authentication from any devices they were logged in. 
    