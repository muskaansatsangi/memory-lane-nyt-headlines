# Memory Lane NYT Headlines Project

This project fetches New York Times headlines for any date, ranks them by importance, and presents the Top 10 headlines in multiple ways:
- Inside Jupyter Notebook
- Downloadable as CSV
- Accessible via a REST API using FastAPI

---

## Project Overview

### Part 1: Fetch and Rank Headlines
- Retrieves articles from the New York Times Archive API  
- Filters results for a chosen date  
- Ranks articles by section (World, U.S., Business, etc.) and article type (News, Front Page)  
- Displays the Top 10 headlines in a clear format  

---

### Part 2: Save Results to CSV
- Optionally save the ranked headlines to a CSV file  
- A clickable download link inside the notebook makes it easy to save to your computer  

---

### Part 3: REST API with FastAPI
- Start a lightweight API directly inside Jupyter Notebook  
- Access headlines in JSON format via a browser or API client:  
  ```
  http://127.0.0.1:8000/headlines?date=YYYY-MM-DD&limit=10
  ```
  (Replace `YYYY-MM-DD` with any date you want)  
- Built-in interactive docs available at:  
  ```
  http://127.0.0.1:8000/docs
  ```

---

## Setup Instructions

### 1. Install dependencies
```bash
pip install fastapi uvicorn requests python-dateutil nest_asyncio python-dotenv
```

### 2. Get a New York Times API key
Sign up at  
https://developer.nytimes.com  

### 3. Create a .env file in the same folder as your notebook
You can create it manually or run this Python code:

```python
with open(".env", "w") as f:
    f.write("NYT_API_KEY=your_key_here\n")
```

Replace `your_key_here` with your actual New York Times API key.

### 4. Run the notebook in order
- Part 1: Fetch and Rank Headlines  
- Part 2: Save to CSV (optional)  
- Part 3: Start REST API (optional)  

---

## Example URLs

- Top 10 headlines for any date:  
  ```
  http://127.0.0.1:8000/headlines?date=YYYY-MM-DD&limit=10
  ```
- Interactive API docs:  
  ```
  http://127.0.0.1:8000/docs
  ```

---

## Notes

- Change `date` and `limit` parameters as needed  
- Project runs entirely on your local machine via Jupyter Notebook  
- Keep your .env file private for security  
