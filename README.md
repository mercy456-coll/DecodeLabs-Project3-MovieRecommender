# 🎬 KorexBot Movie Recommender — AI Recommendation Logic
### DecodeLabs AI Engineering Internship | Project 3 | Batch 2026

---

## 📌 Project Overview

Every time Netflix says "Because you watched…" or Spotify builds your Discover Weekly — that is a recommendation engine at work.

Project 3 moves beyond classification into the world of **AI Recommendation Logic.** Using Content-Based Filtering, TF-IDF Vectorization, and Cosine Similarity, KorexBot Movie Recommender takes your personal interests and matches them against a curated dataset of 25 movies — returning the Top 5 most relevant recommendations with full transparency on why each movie was suggested.

This project proves that personalization does not require massive datasets or neural networks. **Pure mathematical similarity is enough to build something that feels intelligent.**

---

## 🎯 Project Goal

Build a content-based movie recommendation system that:
- Accepts a minimum of 3 user interests as input
- Converts both user profile and movie tags into TF-IDF vectors
- Calculates Cosine Similarity between user profile and all movies
- Sorts and filters results to display Top 5 recommendations
- Shows exactly which interests matched each recommendation

---

## 🎬 Movie Dataset

A curated dataset of **25 movies** spanning multiple genres and cultures:

| Category | Movies |
|---|---|
| 💕 Romance & Emotional | The Notebook, Five Feet Apart, A Walk to Remember, Titanic, Crazy Rich Asians |
| 🔍 Thriller & Mystery | Glass Onion A Knifes Out Mystery, Knives Out, The Housemaid, Smile, Get Out |
| ⚔️ Action & Adventure | Black Panther, Avengers Endgame, RRR, Spider Man No Way Home, Top Gun Maverick, Dune |
| 😂 Comedy & Fun | Roommates, What Men Want, Barbie |
| 🎭 Drama & Inspiration | Parasite, The Woman King, Whiplash |
| 🎌 Animation & Fantasy | KPop Demon Hunters |
| 🌍 International | Squid Game The Movie, Money Heist The Movie |

---

## 🏗️ System Architecture

```
USER INPUT (3+ interests)
        ↓
VALIDATION
— Minimum 3 interests required
        ↓
TF-IDF VECTORIZATION
— User profile → weighted number vector
— Movie tags → weighted number vectors
— Specific words weighted higher than generic ones
        ↓
COSINE SIMILARITY SCORING
— Measures angle between user vector and every movie vector
— Score 1.0 = perfect match
— Score 0.0 = no similarity
        ↓
SORTING
— All 25 movies ranked by similarity score
        ↓
FILTERING
— Top 5 displayed to prevent choice overload
        ↓
OUTPUT
— Movie title + Match Score % + Matched Interests
```

---

## 🧠 Why Content-Based Filtering?

Two types of recommendation systems exist:

| | Collaborative Filtering | Content-Based Filtering |
|---|---|---|
| **How it works** | Finds users similar to you | Matches your profile to item attributes |
| **Needs** | Massive historical user data | Only item metadata and user input |
| **Cold Start Problem** | Fails with new users | Works immediately |
| **Used here** | ❌ | ✅ |

Content-Based Filtering was chosen because it works **immediately** — no historical data needed. It maps preferences directly to item attributes with absolute precision.

---

## 📐 Why Cosine Similarity Over Euclidean Distance?

Euclidean distance measures the straight-line distance between two vectors — making it sensitive to vector magnitude. A movie with many tags would unfairly dominate results.

Cosine Similarity measures the **angle** between two vectors — making it invariant to magnitude. It focuses purely on the **direction** of preferences, not the size.

```
cos(θ) = A·B / (||A|| ||B||)

Score 1.0 → Perfectly aligned (identical interests)
Score 0.0 → Orthogonal (no shared interests)
```

---

## 💻 Sample Output

```
Welcome to KorexBot Movie Recommender!
========================================
Enter your movie interests separated by spaces.
Minimum 3 interests required.
Example: romance comedy thriller fun action

Your interests: animation fantasy adventure

You entered 3 interests: animation fantasy adventure

🎬 Top 5 Movie Recommendations For You:
========================================

1. Barbie
   Match Score: 56.11%
   Matched Interests: animation, fantasy

2. KPop Demon Hunters
   Match Score: 49.06%
   Matched Interests: animation, fantasy

3. Dune
   Match Score: 46.79%
   Matched Interests: fantasy, adventure

4. Avengers Endgame
   Match Score: 22.25%
   Matched Interests: adventure

5. Spider Man No Way Home
   Match Score: 21.79%
   Matched Interests: adventure
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| pandas | Movie dataset organization |
| scikit-learn TfidfVectorizer | Text to weighted vector conversion |
| scikit-learn cosine_similarity | Similarity measurement |
| Jupyter Notebook | Interactive development environment |

---

## 🚀 How to Run

**Step 1 — Install required libraries**
```bash
pip install scikit-learn pandas jupyter
```

**Step 2 — Clone this repository**
```bash
git clone https://github.com/yourusername/DecodeLabs-Project3-MovieRecommender.git
```

**Step 3 — Navigate to the folder**
```bash
cd DecodeLabs-Project3-MovieRecommender
```

**Step 4 — Launch Jupyter Notebook**
```bash
jupyter notebook
```

**Step 5 — Open and run all cells**
```
Project_3_DecodeLabs.ipynb
```

When prompted enter at least 3 interests separated by spaces.

---

## 📂 Project Structure

```
DecodeLabs-Project3-MovieRecommender/
│
├── Project_3_DecodeLabs.ipynb   # Main notebook with full pipeline
└── README.md                    # Project documentation
```

---

## 🔍 Key Concepts Demonstrated

- **Content-Based Filtering** — user preference matched to item attributes
- **TF-IDF Weighting** — specific tags weighted higher than generic ones
- **Cosine Similarity** — angle-based similarity invariant to magnitude
- **Cold Start Bypass** — works immediately with no historical data
- **Top-N Filtering** — prevents choice overload
- **Transparency** — matched interests shown for every recommendation

---

## 📖 What I Learned

Building this recommendation engine taught me that the gap between a simple rule-based system and a personalized AI engine is smaller than most people think. The secret is not complexity — it is **choosing the right mathematical tool for the right problem.**

TF-IDF taught me that not all words are equal. Cosine Similarity taught me that direction matters more than magnitude. And Content-Based Filtering taught me that you can build something genuinely useful without needing anyone else's data.

---

## 🔮 The Bigger Picture

This project sits at the conceptual bridge between:
- **Project 1** — Exact keyword matching (rule-based)
- **Project 3** — Weighted semantic matching (TF-IDF + Cosine)
- **Future** — True semantic understanding (embeddings + neural networks)

Each project is one step up the AI ladder.

---

## 👩‍💻 Built By

**Mercy Inameti**
AI Engineering Intern — DecodeLabs Batch 2026
Project 3 | AI Recommendation Logic

---

*"Before you can build systems that understand meaning, you must master systems that measure similarity." — DecodeLabs*
