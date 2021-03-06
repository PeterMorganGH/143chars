143chars is a Twitter-like website built on Node.js/Express and MongoDB.

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installing](#installing)
- [API](#api)
- [Technologies](#technologies)
- [Acknowledgments](#acknowledgments)

## Features

- Server and Client interface
- User registration/deletion and authentication
- Registered users can send and delete messages
- Basic REST API functions are available with more currently in development

## Getting Started

Want to check out 143chars? Here is what you will need:

### Prerequisites

1. Node.js
2. MongoDB

### Installing

Clone the GitHub repository

```
git clone https://github.com/PeterMorganGH/143chars.git
```

Change to the directory of the cloned respository

```
cd 143chars
```

Install the required packages with npm

```
npm install
```

Create a .env file: Some variables are stored in a special file named ".env". You will need to create the .env file in the project's root directory and make some changes. At the most basic level you will need to add a string for the SESSION_SECRET. You can also change the other values if needed.

```
PORT = 3000
MONGO_URI = mongodb://localhost:27017/143chars
SESSION_SECRET =
```

With MongoDB running, start the application

```
node app.js
```

Visit localhost:3000 in your web browser

## API

| Method | Route                         | Action                             |
| ------ | ----------------------------- | ---------------------------------- |
| GET    | /                             | Retrieve all messages              |
| GET    | /user/:userId                 | Retrieve user's messages           |
| GET    | /user/:userId/settings        | Retrieve user's settings           |
| POST   | /new/user                     | Create new user                    |
| POST   | /new/message                  | Create new message                 |
| POST   | /login                        | Login in user                      |
| DELETE | /delete/message/:messageId    | Delete message                     |
| DELETE | /delete/messages/:userId      | Delete all of user's messages      |
| DELETE | /delete/user/:userId          | Delete user's messages and account |
| PUT    | /user/:userId/settings/update | Update user's settings             |

## Technologies

Project built with:

- [Node.js](https://nodejs.org) - JavaScript server/client
- [Express](https://expressjs.com/) - Web application framework for Node.js
- [MongoDB](https://www.mongodb.com/) - Database
- [Bootstrap](https://getbootstrap.com/) - CSS framework

## Acknowledgments

- SVG Avatars by [SVGRepo](https://www.svgrepo.com)
