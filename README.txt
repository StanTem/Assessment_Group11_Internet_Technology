# A-CRM Web App

This is our Blog Web-App for the Assessment of Internet Technology

Deploy Link Heroku:


#### Contents:
- [Analysis](#analysis)
  - [Scenario](#scenario)
  - [User Stories](#user-stories)
  - [Use Case](#use-case)
- [Design](#design)
  - [Prototype Design](#prototype-design)
  - [Domain Design](#domain-design)
  - [Business Logic Design](#business-logic-design)
  - [Endpoint Design](#endpoint-design)
- [Implementation](#implementation)
  - [Backend Technology](#backend-technology)
  - [Frontend Technology](#frontend-technology)
- [Deployment](#deployment)
- [User Guide](#user-guide)
- [Project Management](#project-management)
  - [Roles](#roles)
  - [Milestones](#milestones)

## Analysis

The application has to be able to provide the user with the information of a fictive cooking course website by a blog. 

### Scenario

Initially it was difficult to find a common idea for the content of the application. Also because two of the 3 group members did not have any basic programming skills nor knowledge. In the beginning we aimed for a fancy visual style website. Allthough the css styles where to hard for the whole team to keep up, we decided to build a simple clean blog website to have everybody involved in the same way.  


### User Stories
1.	As an private person, I want to have a Web app so that I can share my receips on it with different mobile devices and on desktop computers.
2.	As an private person, I want to see a consistent visual appearance so that I can navigate easily, and it looks consistent.
3.	As an private person, I want to use list views so that I can explore and read the published receips.
4.	As an staff member, I want to use edit and create views so that I can maintain my business data.
5.	As an staff member, I want to create an account so that I can get access to the Web app.
6.	As an staff  member, I want to log-in so that I can authenticate myself.
7.	As an staff member, I want to post new notes to the website

### Use Case


![](images/use-case.png


- UC-1 [Post Blog Content]: User and Staff can read and post new blog entries.
- UC-2 [Register into Staff area]: Staff can register an account to get access to school notes.
- UC-3 [Login into staff area]: Staff can login with saved credentials to the staff area.
- UC 4 [Authenticate] Staff has to authenticate at the login as the credentials are encrypted.
- UC-4 [Edit Notes]: Staff can add and delete notes in the staff area.  


## Design

### Prototype Design

The prototype has been designed via nodejs by expanding the application and has been launched on the localhost via mongoose. 

The prototype was designed via a basic html grid and interconnected with a CSS file which was centrally connected by a Java Script app.js document. 

Webfonts where taken partly from font.google.com and implemented.  Further the assets express, EJS, Mongoose and variants of it for the passport generation were used to also connect it later with Robot 3t and Mongodb. 


### Domain Design

The domain is structured as follows:

const userSchema = new mongoose.Schema ({
  email: String,
  password: String,
  googleId: String,
  secret: Strin
});



passport.use(new GoogleStrategy({
    clientID: process.env.CLIENT_ID,
    clientSecret: process.env.CLIENT_SECRET,
    callbackURL: "http://localhost:3000/auth/google/secrets",
    userProfileURL: "https://www.googleapis.com/oauth2/v3/userinfo"
  },



**Method:** `POST`

**Sample Registration of Staff Member

```EJS
<div class="container mt-5">
  <h1>Register</h1>

  <div class="row">
    <div class="col-sm-8">
      <div class="card">
        <div class="card-body">

          <!-- Makes POST request to /register route -->
          <form action="/register" method="POST">
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" class="form-control" name="username">
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input type="password" class="form-control" name="password">
            </div>
            <button type="submit" class="btn btn-dark">Register</button>
          </form>

        </div>
      </div>
    </div>

    <div class="col-sm-4">
      <div class="card">
        <div class="card-body">
          <a class="btn btn-block btn-social btn-google" href="/auth/google" role="button">
            <i class="fab fa-google"></i>
            Sign Up with Google
          </a>
        </div>
    
      </div>
    </div>

  </div>
</div>



**Sample Login of Staff Member


```EJS
<div class="container mt-5">
  <h1>Login</h1>

  <div class="row">
    <div class="col-sm-8">
      <div class="card">
        <div class="card-body">

          <!-- Makes POST request to /login route -->
          <form action="/login" method="POST">
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" class="form-control" name="username">
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input type="password" class="form-control" name="password">
            </div>
            <button type="submit" class="btn btn-dark">Login</button>
          </form>

        </div>
      </div>
    </div>

    <div class="col-sm-4">
      <div class="card">
        <div class="card-body">
          <a class="btn btn-block btn-social btn-google" href="/auth/google" role="button">
            <i class="fab fa-google"></i>
            Sign In with Google
          </a>
        </div>
      </div>
    </div>

  </div>
</div>






**Error Response** • *Code:* `404 NOT FOUND`

## Implementation

### Backend Technology



The webapplication is relying on NodeJS and the following technologies:

EJS (https://ejs.co/)
Mongodb (https://www.mongodb.com/)
Mongoose(https://mongoosejs.com/)
Robot 3t(https://robomongo.org/ )
Postman Express (https://www.postman.com/ )



### Frontend Technology
This Web application is relying on the following frontend technology/libraries:

- EJS
- Bootstrap

## Deployment
This spring boot has been deployed to Heroku.

## User Guide
The Web application can be accessed over the browser by using the following address: `https://***.herokuapp.com/`. And the Swagger-UI can be access using the specific page: `https://***.herokuapp.com/swagger-ui/`.

## Project Management

### Roles
- All-rounder: [Stanil Temelkov]
- Support in research, coordination and testing: [Cil Oguzhan]
- Support in presentation: [Martijn Roozendaal]

### Milestones
1. **Analysis**: Roadmap, research, installation of ressources. 

2. **Frontend Design**: Structure the front end to be nice and clean. 
 
3. **Domain Design**: Definition of domain model.
4. **Backend Design**: Definition of Backend logic

5. **API design and Usecases**: structuring the API generation and planning the implementation

6. **Security and Frontend Implementation**: Integration of security framework and frontend realisation.

7. **Combination**: Putting everything together and launching the app.


