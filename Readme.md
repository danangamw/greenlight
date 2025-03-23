# Greenlight

This is a Go-based API project built using `net/http` for handling requests and responses.

## Features

- RESTful API endpoints
- JSON response handling
- Parameterized URL handling (`/api/movies/:id`)
- Graceful shutdown handling
- Basic rate limiting

## Prerequisites

- Go 1.23 or later
- PostgreSQL (if using a database)
- `curl` (for testing API endpoints)

## Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/danangamw/greenlight.git
   cd greenlight
   ```

2. Initialize the Go module:

   ```sh
   go mod tidy
   ```

3. Run the application:
   ```sh
   go run main.go
   ```

## API Endpoints

| Method | Endpoint          | Description                |
| ------ | ----------------- | -------------------------- |
| GET    | `/api/movies/:id` | Get movie details by ID    |
| POST   | `/api/movies`     | Create a new movie         |
| PATCH  | `/api/movies/:id` | Update movie details by ID |
| DELETE | `/api/movies/:id` | Delete a movie by ID       |

### Example Request

To fetch a movie with ID `1`, use:

```sh
curl -X GET http://localhost:8080/api/movies/1
```

## Project Structure

```
my-go-project/
│── cmd/
│   └── api/
│       ├── main.go
│       ├── routes.go
│       ├── handlers.go
│── internal/
│   ├── data/
│   │   ├── movie.go
│   ├── middleware/
│── go.mod
│── go.sum
│── README.md
```

## License

This project is licensed under the MIT License. See `LICENSE` for more details.
