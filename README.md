# ScholariGo
by Oriyan Nadav
She Codes crowdfunding project - DRF Backend.

## About
Welcome to ScholariGo, the leading crowdfunding platform dedicated to making higher education accessible for all aspiring students! At ScholariGo, our primary purpose is to bridge the financial gap and empower students who dream of pursuing higher education but face financial constraints. We understand the soaring costs of university tuition can be a significant hurdle for many students and their families. That's why we've created ScholariGo, a platform that connects determined students with compassionate individuals, alumni, and organizations who believe in the transformative power of education. Our mission is to ensure that no deserving student is deprived of the opportunity to study at their dream university due to financial limitations. If you are a motivated student seeking to pursue higher education or a generous supporter who believes in the value of education, join ScholariGo today and become part of a community that is shaping brighter futures and unlocking the potential of talented minds. Together, we can break down barriers and pave the way for a more equitable and educated world.

## Features
{{ The features your MVP will include. (Remember this is a working document, you can change these as you go!) }}
* [] Username
* [] Email
* [] Password
* [] Image
* [] Bio


### Stretch Goals
{{ Outline three features that will be your stretch goals if you finish your MVP }}

* [] Commnets section
* [] Update account
* [] Update posts
* [] Delete posts only for creators
* [] Option to get notified about how the post is going (achieved their goal, not yet, close)

## API Specification

| HTTP Method | Url | Purpose | Request Body | Successful Response Code | Authentication <br /> Authorization
| --- | ------- | ------ | ---- | -----| ----|
| GET | /projects/ | Return all projects | N/A | 200 | N/A |
| POST | /projects/ | Create a new project | Project object | 201 | User must be logged in. |
| GET | /projects/1 | Return project with an ID of "1" | Project object | 200 | N/A |
| PUT | /projects/1 | Updates the project with an ID of "1" | Project object | 200 | User must be logged in. User must be the owner of the project. | User must be logged in. User must be the owner of the project. |
| POST | /pledges/ | Create a new pledge | Pledge object | 201 | User must be logged in. User must be the owner of the project. |
| GET | /pledges/1 | Get the pledges with an ID of "1" | N/A | 200 | N/A |
| DELETE | /pledges/1 | Delete the pledges with an ID of "1" | N/A | 200 | User must be logged in. User must be the owner of the project. |

## Database Schema

![Data_base_schema](/screenshots/db_schema.png)

## Wireframes
{{ Insert your wireframes }}

![image info goes here](./docs/image.png)

## Colour Scheme

![image info goes here](/screenshots/Color-Palette.png)

## Fonts
{{ outline your heading & body font(s) }}

## Submission Documentation
{{ Fill this section out for submission }}

Deployed Project: [Deployed website](http://linkhere.com/)

### How To Run
{{ What steps to take to run this code }}

### Updated Database Schema
{{ Updated schema }}

![image info goes here](./docs/image.png)

### Updated Wireframes
{{  Updated wireframes }}

![image info goes here](./docs/image.png)

### How To Register a New User
{{ Step by step instructions for how to register a new user and create a new project (i.e. endpoints and body data). }}

### Screenshots
* [] A screenshot of Insomnia, demonstrating a successful GET method for any endpoint.
![image info goes here](./docs/image.png)

* [] A screenshot of Insomnia, demonstrating a successful POST method for any endpoint.
![image info goes here](./docs/image.png)

* [] A screenshot of Insomnia, demonstrating a token being returned.
![image info goes here](./docs/image.png)












