# News Sentiment App

University project built with FastAPI.

This repository contains the News part of a larger university project. The application receives a list of companies from another backend service, requests related articles from an external news API, evaluates article titles using positive and negative word lists, and exposes the results through REST endpoints and a simple web interface.

## What is included

- FastAPI application
- REST endpoints for stock/news data and recommendations
- Communication with another backend service through HTTP
- External news API integration
- Simple sentiment scoring based on positive and negative word lists
- HTML view with Jinja2 templates
- Automated tests with `pytest`
- FastAPI `TestClient`
- Mocking external HTTP calls with `unittest.mock`
- GitHub Actions CI

## Main endpoints

- `GET /`
- `GET /stocks-data`
- `GET /liststock`
- `GET /recommendations`
- `POST /recommendations`
- `GET /external-stocks`
- `GET /log`

## Project context

The original assignment was split into multiple communicating parts. This repository contains the News service. The second backend service is not included in this repository and is contacted through its REST endpoint.

## Testing

The included tests cover sentiment analysis, word-list loading, mocked external API calls, communication with the other backend service, REST endpoints, filtering, error handling, and log download.

Run:

```bash
pytest
```

The repository also contains a GitHub Actions workflow that runs the tests automatically.

## Configuration

The News API key is read from the `NEWS_API_KEY` environment variable.

Example:

```env
NEWS_API_KEY=your_api_key_here
```

A real API key should not be committed to GitHub.

## Run locally

Install dependencies:

```bash
pip install -r requirements.txt
```

Set `NEWS_API_KEY` in your environment and start the application:

```bash
uvicorn main:app --reload
```

## Technologies

Python, FastAPI, httpx, Jinja2, pytest, GitHub Actions
