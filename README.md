# CRUD back end takehome challenge

Imagine you are a software engineer applying for your first job. You are going to create a back end application so you can keep track of the jobs you apply for and their current status.

You should use only your own code. Do not use ChatGPT or generative AI, and do not copy code from anyone else. If you look up how to do something, cite the URL in a comment next to the code you use.

**I expect you to be able to explain clearly and correctly what every single line of code does in your submission.**

## Getting started
1. Fork this repo.
1. Clone your fork to your machine.
1. run `npm install` to install dependencies, and `npm start` to start the server.
1. Write code to implement the [user stories](#user-stories) and [other requirements](#other-requirements) below.
1. Commit and push your code as you go, ideally one commit per user story or requirement.

## Submitting
When you have completed ALL the [user stories](#user-stories) and [other requirements](#other-requirements) EXACTLY, push all your code to GitHub and open a PR against the upstream repo. (This should be a PR against the repo owned by the `pursuit-nw-accelerator` org, not a PR against your own repo.)

Do not submit until you are confident you have completed ALL the requirements EXACTLY.

Submissions must be posted as a PR by the deadline. Extensions will not be accepted.

## <a id="user-stories"></a> User stories
As a client, I should be able to:
1. Know if the API is up and running by visiting a health check route.
1. See all the job applications I have created.
1. See a specific job application, requested by its id.
1. Create a new job application.
1. Update / change an existing job application.
1. Delete an existing job application.

## <a id="other-requirements"></a> Other requirements
1. Your API should not cause CORS errors in the Google Chrome web browser.
1. All routes should return JSON with the correct status code.
1. Route names and methods follow proper REST conventions (`POST /applications`, not `POST /make_new_application`)
1. For a successful response, return JSON in this format: `{ "data": <data to be returned> }`
1. When there is an error, return JSON in this format: `{ "error": <the actual error message> }`
1. Your application should be organized into a controller layer, a query layer, and middleware.
1. When your server starts, it should listen on a port specified by the `PORT` environment variable. If there is no environment variable, it should listen on port 9000 as a default.
1. Catch all server errors and return the appropriate status code. Do not swallow any errors or error messages.
1. Return the correct error and status code if the application the client wants to read, update, or delete is not found.
1. When a route includes an `id` param, validate that the id can be parsed as a positive integer. Return the correct status code and message if the id is not valid.
1. When creating or updating an application, validate the client's input. Return the correct status code if it's not valid.
    - There must be a company and status
    - The status must be one of the statuses listed in `constants.js`
    - The url field is optional, but should have a `null` value if it isn't present.
    - No other fields should be present (including `id`, `createdAt`, `updatedAt`, `admin`, etc.)
1. Replace this README with a new README file. It must contain the following:
    - A title
    - Your name
    - Detailed, working step by step instructions on how to run the server locally
    - A complete list of methods + routes that your API supports (ex: `GET /students/:id, PUT /students/:id`) 

# Take Home Backend CRUD Operations
## Dennys Antunish
### Follow the below steps to run this project
- open a new directory on your computer (or any folder you wish to have this project in) and then run the command git clone 
- Run the command `code .` to open the repisotry to vscode
- Run the command `npm i express cors nodemon dotenv` to install the neccasry packages to ensure the project runs smoothly
- run the command `nodemon start` and then head to http://localhost:9000/ 

## Routes/Methods
### The below routes + methods are supported on this project
Get All job applications
- GET /students/

Get a job application by id
- GET /students/:id

Create a job application
- POST /students/

Update a job application by id
- PUT /students/:id

Delete a job application by id
- DELETE /students/:id





