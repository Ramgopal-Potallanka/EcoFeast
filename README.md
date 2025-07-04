# Food Management & Recipe Suggestion Platform

## Overview
This project helps users manage food inventory, check expiry status, and discover recipes based on available (non-expired) items. It consists of a Flask backend and a React frontend.

## Features
- Classify food items as "Expired" or "Not Expired" based on purchase date and shelf life.
- Suggest recipes for non-expired items using the Spoonacular API.
- Show step-by-step recipe instructions and related YouTube videos.
- Additional modules: Google Maps integration, Manure Conversion, and more.

---

## Project Structure
```
hack/
  backend/      # Flask API
    app.py
    uploads/
  frontend/     # React app
    src/
    public/
    package.json
```

---

## Backend Setup (Flask)

### Prerequisites
- Python 3.x
- pip

### Installation
1. Navigate to the backend directory:
   ```sh
   cd backend
   ```
2. (Optional) Create a virtual environment:
   ```sh
   python -m venv venv
   # On Windows:
   .\venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set your API keys in `app.py`:
   - Replace `SPOONACULAR_API_KEY` and `YOUTUBE_API_KEY` with your own keys.
5. Run the backend server:
   ```sh
   python app.py
   ```
   The backend will run at `http://127.0.0.1:5000`.

---

## Frontend Setup (React)

### Prerequisites
- Node.js (v16+ recommended)
- npm

### Installation
1. Navigate to the frontend directory:
   ```sh
   cd frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the React app:
   ```sh
   npm start
   ```
   The frontend will run at `http://localhost:3000`.

---

## Usage
- Open your browser at `http://localhost:3000`.
- Use the UI to classify food items, view recipes, and explore other features.
- The frontend communicates with the backend at `http://127.0.0.1:5000`.

---

## API Keys
- The backend requires valid API keys for Spoonacular and YouTube.
- Obtain your keys and update the following variables in `backend/app.py`:
  - `SPOONACULAR_API_KEY`
  - `YOUTUBE_API_KEY`

---

## Backend API
- `POST /classify` — Classifies food items and returns expiry status and recipe suggestions.
  - Request JSON: `{ "food_items": ["milk 2024-06-01", "bread 2024-06-05"] }`
  - Response JSON: `{ "classified_items": [...], "recipes": [...] }`

---

## License
This project is for educational/demo purposes. Please secure your API keys and do not expose them in production. 
