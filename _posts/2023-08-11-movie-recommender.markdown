---
layout: post
title: "Movie Recommender (Node, MongoDB)"
date: 2023-08-11 10:25:45 -0400
categories: jekyll update
---

[Git Repo](https://github.com/chriscklin/movie_recommender)<br>
This is my first Node project. It is a movie recommender API currently consisting of 3 endpoints.

### POST /api/upload

Description: Uploads movie data from a CSV file.

#### Request

- Method: POST
- URL: `/api/upload`
- Headers:
  - Content-Type: `multipart/form-data`
- Body:

csvFile=@path/to/movies.csv



Replace `path/to/movies.csv` with the actual path to your CSV file.

#### Response

- Status Code: 200 OK
- Example Response:
  ```json
  {
    "message": "Data inserted successfully"
  }
  ```

- Status Code: 400 Bad Request
- Example Response:
  ```json
  {
    "error": "No CSV file uploaded"
  }
  ```

- Status Code: 500 Internal Server Error
- Example Response:
  ```json
  {
    "error": "Internal Server Error"
  }
  ```

In this representation, the request body includes the `csvFile` parameter with the `@` symbol indicating the file upload. The response examples demonstrate different status code scenarios and their corresponding JSON responses. Make sure to adjust the content to match your project's actual behavior and responses.

### GET /api/movies

Description: Retrieves a list of movies.

#### Request

- Method: GET
- URL: `/api/movies`

#### Response

- Status Code: 200 OK
  - Example Response:
    ```json
    [
      {
        "title": "Movie 1",
        "genres": ["Genre 1", "Genre 2"],
        "actors": ["Actor 1", "Actor 2"],
        "directors": ["Director 1"],
        "rating": 8.5
      },
      {
        "title": "Movie 2",
        "genres": ["Genre 3", "Genre 4"],
        "actors": ["Actor 3", "Actor 4"],
        "directors": ["Director 2"],
        "rating": 7.9
      }
    ]
    ```

- Status Code: 500 Internal Server Error
  - Example Response:
    ```json
    {
      "error": "Internal Server Error"
    }
    ```

### GET /api/recommend/:targetMovieTitle

Description: Retrieves recommendations based on a target movie title.

#### Request

- Method: GET
- URL: `/api/recommend/:targetMovieTitle`

Replace `:targetMovieTitle` with the title of the movie you want recommendations for.

#### Response

- Status Code: 200 OK
  - Example Response:
    ```json
    {
        "sortedFilteredRecommendations": [
            {
                "title": "Se7en",
                "similarity": 0.40089186286863654,
                "rating": 8.6
            },
            {
                "title": "The Green Mile",
                "similarity": 0.40089186286863654,
                "rating": 8.5
            },
            {
                "title": "The Godfather",
                "similarity": 0.2857142857142857,
                "rating": 9.2
            },
            // ... more recommendations
        ]
    }
    ```

- Status Code: 404 Not Found
  - Example Response:
    ```json
    {
      "error": "Movie not found"
    }
    ```

- Status Code: 500 Internal Server Error
  - Example Response:
    ```json
    {
      "error": "Internal Server Error"
    }
    ```


