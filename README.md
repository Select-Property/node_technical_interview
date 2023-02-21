# Vita Group - Node JS Coding Challenge

Thanks for taking the time to do our node engineering test. The challenge has two parts:

This test is intended to evaluate your skills and knowledge in Node.js development. You are free to use any resources or references you want, except for direct help from others.

You can use any development environment or tools that you feel comfortable with.

----

## Exercise 1: Authentication

Create a simple authentication system with the following endpoints:

* POST /register: Create a new user with the following fields: username, email, password.

* POST /login: Authenticate a user with the following fields: email, password.

* GET /profile: Get the current user's profile. The user must be authenticated to access this endpoint.

* Use JWT tokens for authentication and authorization. The user's password should be stored securely in the database.

----

## Exercise 2: Database Operations

Create a database schema for a simple blog application with the following models:

User: Fields: `username`, `email`, `password`.

Post: Fields: `title`, `content`, `author_id`, `outreach_id`, `created_at`.

Write a script to seed the database with sample data for testing.

Write a function getPostsByAuthor that returns all posts by a given author's username.

The function should accept a username as an argument and return an array of post objects.

Example usage:

```javascript
const posts = getPostsByAuthor('john_doe');
console.log(posts); // Output: [{ title: 'My First Post', content: 'Lorem ipsum dolor sit amet...', author_id: 1, created_at: '2023-02-21T12:34:56.000Z' }, { title: 'My Second Post', content: 'Nullam hendrerit...', author_id: 1, created_at: '2023-02-22T09:12:34.000Z' }]
```

----

## Exercise 3: Testing

Write unit tests for the getPostsByAuthor function from Exercise 2 using any testing library of your choice.

----

## Exercise 4: Request Latency

When we retrieve a blog posts we also need to make an extra request to retreive it's outreach information from a thrid party service. 

Currently this is not a problem with there being such low numbers of blog posts per aurthor, but in the future this may become a problem when we have a larger number of posts. 

The latency per request to the thrid party is unknown. Can you provide any solutions in how we could tackle this problem in the future?

----

## Submission Guidelines

* The zip file should be named {yourname}.zip, and should itself contain the node tech test project folder with your submission.

* The zip file should contain the [FOLLOW-UP.md](./FOLLOW-UP.md) file with answers to the follow-up questions.

* The zip file should **not** include the `node_modules` folder. (If Applicable)
