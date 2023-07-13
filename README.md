# 🎬 MovieCine 🎬
MovieCine is an API service built with Django Ninja that allows the user to manage a cinema program. It enables adding new movies, updating their status and ranking, and provides a mechanism to display trending movies. Data is stored in a Postgres database and synchronized to MongoDB for querying. The project uses Celery for task management and Redis and RabbitMQ for message passing.

## 🛠 Tech Stack
* 🐍 Django Ninja
* 🐘 Postgres
* 🍃 MongoDB
* 🥬 Celery
* 📕 Redis
* 🐇 RabbitMQ
* 🐳 Docker

  ## 🚀 Getting Started
  
1. Clone the repo:
   ```
   git clone https://github.com/your-github-user/MovieCine.git
   cd MovieCine
   ```
2. Setup Environment Variables:
   Create a .env file in the root directory and setup your environment variables. Example:
   ```
   POSTGRES_USER=postgres
   POSTGRES_PASSWORD=yourpassword
   POSTGRES_DB=movies_db
   MONGODB_URI=mongodb://mongo:27017/movies_db
   REDIS_URL=redis://redis:6379/0
   RABBITMQ_DEFAULT_USER=user
   RABBITMQ_DEFAULT_PASS=password
   ```
3. Start the project:
   ```
   docker-compose up --build -d
   ```
## 📘 API Endpoints
Note: Refer to the swagger documentation available at localhost:8000/docs for detailed API endpoint information.

* POST /movies - Add a new movie
* GET /movies/trending - Get list of trending movies
* ...

## ⚙️ Running Tests
To run the tests, use the following command:
```
docker-compose exec web pytest
```
  
