# 🎬 Movie Recommendation System

A content-based Movie Recommendation System built with Python and machine learning that recommends movies based on movie metadata and textual similarity. The project uses TF-IDF vectorization and precomputed similarity-related artifacts to support movie recommendations through a Python application and API.

## 🚀 Live Demo

🎬 **[Movie Recommendation System — Try it Live](https://movie-recommendation-system-yfcytpc6q4b9ipsvjjzgsi.streamlit.app/)**
- **API Documentation:** [Explore API Docs](https://movie-recommendation-system-92lu.onrender.com/docs)

## ✨ Features

- 🎥 **Content-Based Recommendations:** Recommends movies based on similarities in their metadata.
- 🧠 **TF-IDF Vectorization:** Converts textual movie information into numerical features.
- 🔍 **Similarity-Based Retrieval:** Uses precomputed artifacts to support efficient recommendation lookups.
- 🗂️ **Movie Metadata Processing:** Works with a movie metadata dataset.
- ⚡ **FastAPI Backend:** Provides a framework for exposing recommendation functionality through HTTP endpoints.
- 📚 **Interactive API Documentation:** Explore and test available endpoints using Swagger UI.
- ☁️ **Cloud Deployment:** Backend deployed on Render.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Language | Python |
| Machine Learning | Scikit-learn, TF-IDF |
| Data Processing | Pandas |
| Backend API | FastAPI |
| ASGI Server | Uvicorn |
| Data Storage | Pickle (`.pkl`) artifacts, CSV |
| Deployment | Render |
| Version Control | Git, GitHub |

## 🧠 How It Works

1. **Movie Metadata:** The system uses movie information stored in a CSV dataset.
2. **Text Processing:** Movie text is transformed into numerical features using TF-IDF.
3. **Similarity Artifacts:** Precomputed feature and index artifacts are loaded by the application.
4. **Recommendation Retrieval:** The system uses the saved artifacts to identify relevant movie recommendations.
5. **API Access:** The backend exposes application functionality through FastAPI endpoints.

## 📂 Project Structure

```text
Movie-Recommendation-System/
│
├── app.py
├── main.py
├── requirements.txt
├── movies_metadata.csv
├── df.pkl
├── indices.pkl
├── tfidf.pkl
├── tfidf_matrix.pkl
├── Movie_Recommendation_System.ipynb
├── .gitignore
└── .python-version
```

### File Descriptions

- `app.py` — Application interface or entry point.
- `main.py` — Backend application and API entry point.
- `requirements.txt` — Python dependencies.
- `movies_metadata.csv` — Movie metadata dataset.
- `df.pkl` — Serialized DataFrame used by the project.
- `indices.pkl` — Saved movie index mappings.
- `tfidf.pkl` — Saved TF-IDF vectorizer.
- `tfidf_matrix.pkl` — Precomputed TF-IDF feature matrix.
- `Movie_Recommendation_System.ipynb` — Jupyter notebook for experimentation and development.
- `.python-version` — Specifies the Python version for deployment.

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.11
- Git
- pip

### 1. Clone the Repository

```bash
git clone https://github.com/MousumiBadyakar/Movie-Recommendation-System.git
cd Movie-Recommendation-System
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

**macOS/Linux:**

```bash
python3.11 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Run the Backend

```bash
uvicorn main:app --reload
```

Open the following URL in your browser:

- API: http://127.0.0.1:8000
- Interactive documentation: http://127.0.0.1:8000/docs

To run the interface in `app.py`, use the appropriate command for the framework configured in that file.

## ☁️ Deployment on Render

The backend is hosted on Render.

To deploy your own instance:

1. Push the project to a GitHub repository.
2. Create a new Web Service on Render.
3. Connect your GitHub repository.
4. Select Python 3.11 as the runtime version.
5. Set the build command:

   ```bash
   pip install -r requirements.txt
   ```

6. Set the start command:

   ```bash
   uvicorn main:app --host 0.0.0.0 --port $PORT
   ```

7. Deploy the service and review the build logs.
8. Test the API using the `/docs` endpoint.

Ensure that all required `.pkl` artifacts are available in the deployed environment and that dependency versions are compatible.

## 🔮 Future Enhancements

- Improve movie search and filtering.
- Add movie posters, ratings, genres, and descriptions.
- Integrate an external movie database API for additional movie information.
- Build a polished, responsive user interface.
- Add automated tests for recommendation logic and API endpoints.
- Improve recommendation quality using additional content features or hybrid recommendation techniques.

## 👩‍💻 Author

**Mousumi Badyakar**