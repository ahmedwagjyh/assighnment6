MongoDB Node.js Project

Description

This project is a Node.js REST API built with Express.js and MongoDB.

The project uses a modular folder structure and supports different environments through environment variables.

Technologies

- Node.js
- Express.js
- MongoDB
- MongoDB Node.js Driver
- dotenv
- cross-env

Project Structure

lap/
├── src/
│   ├── common/
│   │   └── utils/
│   ├── DB/
│   │   ├── connection.db.js
│   │   └── model/
│   ├── middleware/
│   ├── modules/
│   │   ├── authentication/
│   │   ├── blog/
│   │   ├── product/
│   │   └── user/
│   └── main.js
├── .env.development
├── .env.production
├── package.json
└── package-lock.json

Installation

npm install

Environment Variables

The project uses two environment files:

- ".env.development"
- ".env.production"

Example:

PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/lap_db
NODE_ENV=development

Run the Project

Development

npm run dev

Production

npm run prod

The server runs on:

http://localhost:5000

API Routes

Authentication

POST /auth/signup
POST /auth/login

Users

GET    /user
GET    /user/:id
POST   /user
PUT    /user/:id
DELETE /user/:id

Products

GET    /product
GET    /product/:id
POST   /product
PUT    /product/:id
DELETE /product/:id

Blog

GET /blog

MongoDB Queries

The project also contains "mongoQuery.txt", which includes MongoDB operations such as:

- Creating collections
- Collection validation
- Creating indexes
- Inserting documents
- Updating documents
- Finding documents
- Sorting, skipping, and limiting results
- Deleting documents
- Aggregation
- "$unwind"
- "$lookup"
- Query operators such as "$gte", "$lte", "$nin", and "$type"

Database Connection

MongoDB is connected using the official MongoDB Node.js driver.

The application automatically selects the environment file based on "NODE_ENV".

npm run dev  → .env.development
npm run prod → .env.production

Error Handling

The project includes a global error-handling middleware to handle errors and return appropriate responses.

Author

Ahmed Wageeh
