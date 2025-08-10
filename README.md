# MoviesDatabase API Project

## API Overview

The MoviesDatabase API provides a comprehensive collection of information for movies, TV shows, and actors. It includes YouTube trailer URLs, awards, full biographies, and many other useful details. The API covers over **9 million titles** (movies, series, and episodes) and **11 million actors/crew members**, offering complete and regularly updated data:

- Titles updated weekly
- Ratings and episodes updated daily
- All endpoints return an object with a `results` key
- Paginated endpoints include `page`, `next`, and `entries` keys
- All query parameters are **optional**

Support the developers: [Buy Me a Coffee](https://www.buymeacoffee.com/SAdrian13)

## Version

Current version as provided in the documentation: **v1**

## Available Endpoints

Below are the main endpoints and their purposes (all parameters optional):

- **`/titles`** – Retrieve a list of titles (movies, series, episodes)
- **`/titles/{id}`** – Get detailed information for a specific title
- **`/titles/search`** – Search for titles by keyword
- **`/titles/{id}/crew`** – Get crew and cast information for a title
- **`/actors/{id}`** – Get full biography and career info for an actor
- **`/trailers/{id}`** – Retrieve YouTube trailer URL for a given title

## Request and Response Format

**Example Request:**

```bash
GET https://moviesdatabase.p.rapidapi.com/titles
Headers:
  X-RapidAPI-Key: YOUR_API_KEY
  X-RapidAPI-Host: moviesdatabase.p.rapidapi.com


**Example Request:**
{
  "results": [
    {
      "id": "tt1234567",
      "title": "Example Movie",
      "year": 2024,
      "trailer_url": "https://youtube.com/watch?v=example",
      "rating": 8.5
    }
  ],
  "page": 1,
  "next": 2,
  "entries": 50
}
```
Authentication
Requests require authentication via RapidAPI:

X-RapidAPI-Key: Your unique API key from RapidAPI

X-RapidAPI-Host: moviesdatabase.p.rapidapi.com

Error Handling
Common error responses:

401 Unauthorized – Invalid or missing API key

404 Not Found – Endpoint or resource not found

429 Too Many Requests – Rate limit exceeded
Handle errors by checking the response status and logging or displaying appropriate error messages.

Usage Limits and Best Practices
RapidAPI usage limits depend on your subscription plan — check your account for quota details

Use pagination to limit large data requests

Avoid excessive requests in a short period to prevent hitting rate limits

Cache frequent queries to reduce API calls and improve performance
