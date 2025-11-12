# Music Recommender System
### An AI-Driven Hybrid Recommendation Engine

---

## 🎵 Introduction

This project is an **AI-driven Hybrid Music Recommendation System** developed to provide personalized music suggestions to users based on their historical preferences and listening behavior.

Leveraging a sophisticated combination of **Collaborative Filtering** and **Content-Based Filtering** techniques, the system effectively addresses the "information overload" challenge prevalent in major digital music platforms. The core objective is to significantly enhance user satisfaction and retention by accurately predicting and recommending engaging songs.

The system was developed as part of an International Research Internship spanning from December 2023 to March 2024, in collaboration between **UCSI University, Malaysia**, and **Sir Padampat Singhania University, India**.

---

## ⚙️ Methodology: The Hybrid Approach

The model utilizes a hybrid strategy for optimal performance:

### Collaborative Filtering
Identifies patterns and similarities among different users or items (songs) by leveraging algorithms such as **Singular Value Decomposition (SVD)**, **K-Nearest Neighbors (KNN)**, and **K-Means Clustering**. This enhances recommendations based on the collective behavior of users with analogous tastes.

### Content-Based Filtering
Analyzes the intrinsic characteristics of songs (including lyrics, genre, and tempo). It employs **Cosine Similarity with a Count Vectorizer** on textual features, fine-tuning suggestions to match individual user preferences precisely.

The integration of these methods ensures superior precision and adaptability compared to traditional single-method recommenders.

---

## 🛠️ Technology Stack

| Category | Technology / Library | Role in Project |
| :--- | :--- | :--- |
| Language | Python 3.x | Core development language. |
| Frontend/UI | Streamlit | Used for rapidly building and deploying the interactive web application interface. |
| Data Science | `pandas`, `scikit-learn` | Data manipulation, processing, and implementation of machine learning algorithms. |
| Core Libraries | `pickle` | Serialization and deserialization of the trained model components (`df.pkl`, `similarity.pkl`). |
| External API | Spotipy (Spotify API) | Used to fetch rich metadata, such as album cover art and song links, for recommendations. |
| Text Processing | NLTK (PorterStemmer) | Used for Natural Language Processing algorithms to analyze song text and lyrics. |

---

## 📂 Project Structure & File Contents

The repository is organized to separate the model development pipeline, the final application, and all supporting research documentation.

| File / Folder | Type | Description |
| :--- | :--- | :--- |
| `app.py` | Python Script | The live Streamlit application. Loads pre-trained models and executes the `recommend()` logic. |
| `Model Training.ipynb` | Jupyter Notebook | Contains the full data pipeline: data loading, cleaning, feature extraction (TfIdVectorizer), and model training. |
| `df.pkl` | Model Asset | Serialized (pickled) DataFrame of processed song information, used by `app.py`. |
| `similarity.pkl` | Model Asset | Serialized (pickled) matrix containing the pre-computed cosine similarity scores. |
| `spotify_millsongdata.csv` | Dataset | The raw song dataset used for training the recommendation model. |
| `Research_Internship_Report_2024.docx` | Documentation | The comprehensive final report detailing objectives, literature review, methodology, and findings. |
| `Research Internship.pptx` | Documentation | Primary presentation slides summarizing the project for stakeholders or academic review. |
| `Results of the Model.docx` | Documentation | Specific findings on model evaluation, NLP algorithms, and prototype implementation. |
| `Research/` (Folder) | Documentation | Directory containing relevant literature review and research papers (.pdf files). |

---

## 🚀 Quick Start (Local Setup)

To run the recommendation system locally, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git](https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git)
    cd YOUR-REPOSITORY-NAME
    ```

2.  **Install Dependencies:**
    *(If a `requirements.txt` file is present, you can simply run `pip install -r requirements.txt`)*
    ```bash
    pip install streamlit pandas scikit-learn spotipy nltk
    ```

3.  **Configure API Keys:**
    * Obtain a **Client ID** and **Client Secret** from the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/).
    * Open `app.py` and update the placeholder values with your actual credentials.

4.  **Run the App:**
    ```bash
    streamlit run app.py
    ```
    The application will open in your default web browser.
