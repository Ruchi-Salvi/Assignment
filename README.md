
## Overview  
This is a Flask-based API that scrapes technical courses from [Brainlox](https://brainlox.com/courses/category/technical) and provides search functionality using TF-IDF and cosine similarity.  

## Features  
- **List all courses**: Fetches and returns a list of course names from Brainlox.  
- **Search for courses**: Allows users to find relevant courses based on a query using TF-IDF similarity.  
- **Health check**: Ensures the API is running.  

## Technologies Used  
- **Python** (Flask, Requests, BeautifulSoup)  
- **Machine Learning** (TF-IDF Vectorization, Cosine Similarity)  

## Installation  

1. Clone the repository:  
   ```sh
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Install dependencies:  
   ```sh
   pip install -r requirements.txt
   ```

3. Run the API:  
   ```sh
   python scraping.py
   ```

## API Endpoints  

### 1. List All Courses  
- **Endpoint**: `GET /list_courses`  
- **Response**: JSON list of course names  

### 2. Search Courses  
- **Endpoint**: `POST /search`  
- **Request Body**:  
  ```json
  {
    "query": "machine learning"
  }
  ```
- **Response**: JSON list of matching courses  

### 3. Health Check  
- **Endpoint**: `GET /health`  
- **Response**:  
  ```json
  {
    "status": "API is running!"
  }
  ```

## Notes  
- Ensure that Brainlox’s website structure remains unchanged for the scraper to function correctly.  
- Update HTML selectors if Brainlox updates its website.  
- Run the Flask app with `debug=True` only in development.  
