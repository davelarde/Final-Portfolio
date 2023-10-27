## Backend Project
Give a high-level overview of the project purpose
- This project are for people who are new in town and are looking for events to meet new friends. Whether is a simple gathering or a big event. The job that will do for them is to be able to meet new people, by allowing them to see posts from everyone to events, bbqs or simply dinners but this application will also allow users to create their own event.
What inspired me to create this application was because I moved to a different city, and sometimes is very hard to meet people when you are completely new in town. The most important features of this application are the creation of vites(events), and be able to see the vites(events) from everyone. Some future features to be implented are to be able to RSVP the event and upload photos.
- STAR Interview Questions:
    - (Situation) Describe the application and why you created this program
        * This is a back-end application built with Node.js and using different request routes, to be able to see all events, create new events, delete events, and also be able to become an admnistrator and have it's own authorization. This application has accesibility only if the user had registered or created their account. Only with an account users will be able to create events and see the rest of the events to be part of NewBee.
    - (Task) Describe the overall structure of your application and the design process prior to building the program
        * This project structure is the following:
        *  DB folder : where all the database created is located and user and vite model. 
        * This folder will make possible to use GET request and POST request to create a new "vite".
        * Public Folder : Will contain all the html files, for the front-end, this was built more for design porpuses to have an actual page and not only be able to tested in Postman only
        * index.js file: 
        Will contain all the main code, where all the routes and logic is located.
    - (Action) Explain the code you wrote to achieve your desired result
        To achieve this application I followed the next steps:
        * First create a database for all vites and users
        * Create User and Vite model to be able to use it with sequelize.
        * Create associations
        * Create sequelize connections
        * Created a seed function to render db.
        * SeedData.js will contain all the seed data that will be used to for the application.
        * index.js in the root folder followed the next steps:
        * It has different requests that will be connected to their according HTML files for example:
        * app.get("/welcome") is related to the dashboard after the user is able to log in into the page.
        *  This code will also have two IMPORTANT POST requests for "login" and "register" where together with an authorization         middleware will grab a token to tested in postman, and for the front-end will have it as a authorization header.
        * There are two types of authorization middleware :
        * administrator authorization middleware
        * setUser authorization middleware for all routes
        * All routes, will adapt the authorization middleware according to it's porpuse. 
        * All User Routes, will only have administrator authorization middleware access.
        * User will be able to GET all VITES, POST(create)new vites, Delete and upate any vite.

    - (Result) Showcase your final application with its functionality
        * The result was a full stack project, where it wouldn't be succesfully be tested in Postman, but user had the chance to see a GUI of how eventually the application would look like.

## Demo
Please find below a quick video on how this app works. 


[Newbee](https://www.youtube.com/watch?v=USKBqCBWP3I)

## Technologies
- Node.js
- SQL
- JWT
- ENVIRONMENTAL VARIABLES with dotenv
- POSTMAN
- SEQUELIZE
- HTML
- CSS
- BCRYPT
- CORS


## Competencies
### Effective implementation of Authorization middleware.
Developed and integrated robust authorization middleware to ensure secure user interactions and administrative functionalities.
- Designed and implemented "setUser" authorization middleware, enabling registered and logged-in users to create, update and delete their own events.
- Developed administrator authorization middleware, allowing ONLY administrators to delete any events, including those created by users and granting them the ability to add users as administrators.
- Ensured a secure environment where user actions were restricted based on their roles enhancing overall system integrity and user privacy.


### Seamless integration of backend functionality with frontend
Successfully connected backend functionality to the frontend, overcoming challenges related to bearer token authentication.
- Implemented all backend routes(user registration/login,vite creation, updating and delete)to function correctly, ensuring the application's core logic was sound and reliable.
- Overcame difficulties in connecting the backend with the frontend by understanding and implementing bearer token authentication, allowing secure data transmission and user authentication.
- Rigorously tested the backend endpoints in Postman, ensuring all functionalities worked as intended, and succesfully integrated them with the frontend, ensuring a seamless and responsive user experience.
- Learned how to pass the bearer token into the authentication header, so it can be succesfully connected to the frontend.
