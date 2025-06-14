#  Movie API

A simple and efficient **Movie API** built with **Node.js**, **Express**, and **SQLite (better-sqlite3)**. This API serves movie data with support for filtering by year and genre, and includes pagination. Also comes with robust **Jest tests** to ensure endpoint reliability.


##  Features

-  List all movies (paginated)
-  Get movie details by IMDb ID
-  Filter movies by release year (with optional sort)
-  Filter movies by genre
-  Budget displayed in dollars
-  Fully tested with **Jest** and **Supertest


##  Tech Stack

- **Node.js**
- **Express.js**
- **SQLite** (using `better-sqlite3`)
- **Jest** & **Supertest** for testing


##  Project Structure

movie-api/
├── controllers/
│ └── movieController.js # Main API logic
├── config/
│ ├── db.js # SQLite connection (main DB)
│ └── dbRatings.js # Separate connection for ratings
├── routes/
│ └── movieRoutes.js # Route definitions
├── tests/
│ └── movieController.test.js# Jest test file for all endpoints
├── app.js # Express app setup (if applicable)
├── package.json
└── README.md

##  Setup Instructions

Install dependencies
npm install
Run the server
node app.js
# Or with nodemon
npm run dev

🌐 API Endpoints
Method	Route	Description
GET	/movies	Get all movies (paginated, 50/page)
GET	/movies/:imdbid	Get movie details by IMDb ID
GET	/movies/year/:year	Filter movies by release year
GET	/movies/genre/:genre	Filter movies by genre

🔍 Query Parameters
page: Page number (defaults to 1)

sort: For /year/:year, accepts asc or desc

🧪 Run Tests
This project includes Jest tests to validate all controllers.


npm test
Example test coverage:

✅ Movies list

✅ Movie by ID

✅ Movies by year (valid/invalid)

✅ Movies by genre

✅ Error responses (e.g., 404, 400)

📝 Sample .env (if needed for DB path)
If you move to using an .env file:


DB_PATH=./db/movies.sqlite
DB_RATINGS_PATH=./db/ratings.sqlite
Then modify config/db.js and config/dbRatings.js to read from it using dotenv.




