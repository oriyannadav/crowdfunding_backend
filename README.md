# Schoolr
by Oriyan Nadav
She Codes crowdfunding project - DRF Backend.

## About

Welcome to Schoolr, the leading crowdfunding platform dedicated to making higher education accessible for all aspiring students! At Schoolr, our primary purpose is to bridge the financial gap and empower students who dream of pursuing higher education but face financial constraints. We understand the soaring costs of university tuition can be a significant hurdle for many students and their families. That's why we've created Schoolr, a platform that connects determined students with compassionate individuals, alumni, and organizations who believe in the transformative power of education. Our mission is to ensure that no deserving student is deprived of the opportunity to study at their dream university due to financial limitations. If you are a motivated student seeking to pursue higher education or a generous supporter who believes in the value of education, join Schoolr today and become part of a community that is shaping brighter futures and unlocking the potential of talented minds. Together, we can break down barriers and pave the way for a more equitable and educated world.

## Features

* [x] Have a clear target audience.
* [x] Have user accounts. A user should have at least the following attributes:
    * [x] Username
    * [x] Email address
    * [x] Password
* [x] Ability to create a “project” to be crowdfunded which will include at least thefollowing attributes:
    * [x] Title
    * [x] Owner (a user)
    * [x] Description
    * [x] Image
    * [x] Target amount to fundraise
    * [x] Whether it is currently open to accepting new supporters or not
    * [x] When the project was created
* [x] Ability to “pledge” to a project. A pledge should include at least the followingattributes:
    * [x] An amount
    * [x] The project the pledge is for
    * [x] The supporter/user (i.e. who created the pledge)
    * [x] Whether the pledge is anonymous or not
    * [x] A comment to go along with the pledge
    * [x] Implement suitable update/delete functionality, e.g. should a project owner be allowed to update a project description?
* [x] Implement suitable permissions, e.g. who is allowed to delete a pledge?
* [x] Return the relevant status codes for both successful and unsuccessful requeststo the API.
* [ ] Handle failed requests gracefully (e.g. you should have a custom 404 page rather than the default error page).
* [x] Use Token Authentication.
* [ ] Implement responsive design

### Stretch Goals

* [x] Update user details
* [x] Update posts
* [x] Delete posts/pledges only for creators
* [x] A user can delete themselves 
* [] Option to get notified about how the post is going (achieved their goal, not yet, close)- frontend

## API Specification

| HTTP Method | Url | Purpose | Request Body | Successful Response Code | Authentication <br /> Authorization
| --- | ------- | ------ | ---- | -----| ----|
| GET | /users/ | Return all uers | N/A | 200 | N/A |
| POST | /uers/ | Create a new users | Project object | 201 | N/A |
| PATCH | /users/1 | Updates the user with an ID of "1" | Project object | 201 | User must be logged in. | User must be logged in. |
| DELETE | /users/1 | Delete the user with an ID of "1" | N/A | 200 | User must be logged in. Pk should be logged in user. |
| GET | /projects/ | Return all projects | N/A | 200 | N/A |
| POST | /projects/ | Create a new project | Project object | 201 | User must be logged in. |
| GET | /projects/1 | Return project with an ID of "1" | Project object | 200 | N/A |
| PUT | /projects/1 | Updates the project with an ID of "1" | Project object | 200 | User must be logged in. User must be the owner of the project. | User must be logged in. User must be the owner of the project. |
| DELETE | /projects/1 | Delete the project with an ID of "1" | N/A | 200 | User must be logged in. User must be the owner of the project. |
| POST | /pledges/ | Create a new pledge | Pledge object | 201 | User must be logged in. User must not be the owner of the project. |
| GET | /pledges/1 | Get the pledges with an ID of "1" | N/A | 200 | N/A |
| DELETE | /pledges/1 | Delete the pledges with an ID of "1" | N/A | 200 | User must be logged in. User must be the owner of the pledge. |

## Database Schema

![Data_base_schema](/screenshots/db_schema.png)

## Wireframes
![Wireframes](/screenshots/wireframe.png)

## Colour Scheme

![Colour_scheme](/screenshots/Color-Palette.png)

## Fonts

* Heading - Montserrat (typeface)
* Body - Raleway

## Submission Documentation

Deployed Project: [Deployed website](https://schoolr.fly.dev/projects/)

![Deployed website](/screenshots/deployed-website1.png)
![Deployed website](/screenshots/deployed-website2.png)

<!-- ### Updated Wireframes
{{  Updated wireframes }}

![image info goes here](./docs/image.png) -->

### How To Register a New User

To begin, you can register a new user by sending a POST request to "https://schoolr.fly.dev/users/", including the desired username and password in the JSON body. Next, obtain a user token by using another POST request at "https://schoolr.fly.dev/api-token-auth/", providing the username and password in the JSON body to receive the token. With the token in hand, you can create a new project by sending a POST request to "https://schoolr.fly.dev/projects/". In the request's Authorization header, select "Bearer Token" and enter the previously obtained token in the "Token" section, prefixing it with "Token". In the JSON body of the request, provide details such as the project's title, description, goal, image, openness status, and creation date. This sequence of steps guides you through user registration, token acquisition, and project creation seamlessly.

### Screenshots
* [x] A screenshot of Insomnia, demonstrating a successful GET method for any endpoint.
![Get_request](/screenshots/get-request.png)
![Get_request2](/screenshots/get-request2.png)

* [x] A screenshot of Insomnia, demonstrating a successful POST method for any endpoint.
![Post_request](/screenshots/post-request.png)

* [x] A screenshot of Insomnia, demonstrating a token being returned.
![User-token](/screenshots/user-token.png)