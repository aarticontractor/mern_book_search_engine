# mern_book_search_engine


## Description

[Visit the Deployed Site](https://book-search-aarti.herokuapp.com/)
<br>
 I have taken a fully functioning Google Books API search engine built with a RESTful API, and refactored it to be a GraphQL API built with Apollo Server. The app was built using the MERN stack, with a React front end, MongoDB database, and Node.js/Express.js server and API.
 To fulfill the challenge, I have done the following:

- Set up an Apollo Server to use GraphQL queries and mutations to fetch and modify data, replacing the existing RESTful API.

- Modified the existing authentication middleware so that it works in the context of a GraphQL API.

- Created an Apollo Provider so that requests can communicate with an Apollo Server.

- Deployed the application to Heroku.

<br>
<br>


## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:|    
| Git | [https://git-scm.com/](https://git-scm.com/)     |  
| JavaScript | [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) |  
| NodeJs | [https://nodejs.org/en](https://nodejs.org/en) |
| ExpressJS | [https://www.npmjs.com/package/express](https://www.npmjs.com/package/express) |
| GraphQL | [https://graphql.org/](https://graphql.org/) |
| MongoDB | [https://www.mongodb.com/](https://www.mongodb.com/) |
| Mongoose ODM | [https://www.npmjs.com/package/mongoose](https://www.npmjs.com/package/mongoose) |
| Apollo Server | [https://www.apollographql.com/docs/apollo-server/](https://www.apollographql.com/docs/apollo-server/) |
| React | [https://react.dev/](https://react.dev/) |

<br>
<br>


## Table of Contents

* [Installation](#installation)
* [Application Highlights and Usage](#application-highlights-and-usage)
* [Code Snippets](#code-snippets)
* [Learning Points](#learning-points)
* [Author Info](#author-info)
* [Credits](#credits)

<br>
<br>


## Installation

The 'MERN Book-Search-Engine' requires installation of mongoDB, and express-js and mongoose NPM packages.
 After cloning down the repository, go to the command-line in the terminal and do an 'npm install' to install all the dependencies stated in the 'package.json' file and run 'npm run start' or 'npm run develop' to start the server on both client and server side.
<br>
<br>
<br>

## Application Highlights and Usage
<br>


1. The below Gif demonstrates the functionality of the application where the user can sign up, login in and browse books, save them in their account, delete the saved book, and logout:

<br>
<br>

![alt text](./client/src/images/app-functionality.gif)



## Code Snippets

<br>

 The following code snippet shows how the Apollo client has been setup in the server.js:

```javascript
const server = new ApolloServer({
  typeDefs,
  resolvers,
  context: authMiddleware
});
```

<br>
<br>

The following code snippet shows an example of a mutation for user Login:


```javascript
import { gql } from '@apollo/client';

export const LOGIN_USER = gql`
  mutation login($email: String!, $password: String!) {
    login(email: $email, password: $password) {
      token
      user {
        _id
        username
        email
      }
    }
  }
`;
```



## Learning Points 

   I learned the following skills while doing this project:
<br>
- Java script basics (variables,functions, arrays, for-loops, if-else etc)
- Basics of NodeJs server and related functions
- How to write API routes with MongoDb as the database instead of using MySQL queries
- Using the express and mongoose packages from NPM 
- Creating collections using MongoDB and their associations to create relationships between collections using mongoose.
- Using GraphQL queries and testing them in Playground
- How to build a MERN stack application and implementing React for UI.


<br>
<br>

## Author Info

### Aarti Contractor


- Portfolio: https://aarticontractor.github.io/aarticontractor_portfolio/
- Linkedin: https://www.linkedin.com/in/aarti-contractor/
- Github: https://github.com/aarticontractor

<br>

## Credits

- https://developer.mozilla.org/en-US/docs/Web/JavaScript
- https://cloudconvert.com/webm-to-gif
- https://nodejs.org/en
- https://www.npmjs.com/package/express
- https://www.mongodb.com/
- https://www.npmjs.com/package/mongoose
- https://graphql.org/
- https://react.dev/
- https://www.apollographql.com/docs/apollo-server/


<br>

© 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.