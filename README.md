# StartFundr
by Oriyan Nadav
She Codes crowdfunding project - DRF Backend.

## About
Welcome to StartFundr, the crowdfunding platform dedicated to empowering small local businesses and startups! Our core purpose is to provide an accessible and user-friendly platform that enables entrepreneurs to raise funds and turn their visions into successful ventures. Whether you're a budding entrepreneur with a brilliant concept or an existing local business looking to expand your operations, StartFundr is here to support you every step of the way. We understand that securing funding can be challenging, especially for startups and local businesses, which is why we've designed StartFundr to be a hub for connecting passionate entrepreneurs with a community of enthusiastic backers. By harnessing the collective power of the crowd, we aim to foster innovation, drive economic growth, and create opportunities for businesses to thrive. Join StartFundr today and witness the magic of collective support transforming dreams into reality.

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












