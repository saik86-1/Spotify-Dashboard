# Spotify-Dashboard

# Top 10 Artists of 2024 — Spotify (Tableau Dashboard)

A clean, interactive Tableau dashboard spotlighting the **10 most-streamed artists on Spotify in 2024**, plus each artist’s top track.

<img width="1659" height="994" alt="image" src="https://github.com/user-attachments/assets/3a9f2c35-fd13-4600-8e76-3c1139e4b835" />

---

## Features
- **Top 10 Artists (Bar Chart)** — ranked by total Spotify streams in 2024  
- **Top Track per Artist (Table)** — the highest-streamed track for each top artist  
- **Highlight Track** — dropdown to spotlight a song across views  

---

## Data
**File:** Uplaoed on the Repository

**Minimum columns:**
- `Track`, `Album Name`, `Artist`, `Release Date`
- `Spotify Streams`, `Spotify Playlist Count`, `Spotify Playlist Reach`, `Spotify Popularity`

---

## How Rankings Are Computed
1. **Total streams per artist (2024):** `SUM([Spotify Streams])` for tracks released in 2024  
2. **Top-10 selection:** sort artists by total streams  
   - ties → higher `Spotify Playlist Reach`, then higher `Spotify Popularity`  
3. **Top track per artist:** pick, in order of priority  
   1) highest `Spotify Streams`  
   2) higher `Spotify Playlist Reach`  
   3) higher `Spotify Popularity`  
   4) earliest `Release Date`

---

---

## Notes
- Public Spotify datasets vary in coverage; this project treats the provided CSV as the source of truth  
- Cross-platform comparisons (Apple/YouTube/etc.) are **out of scope**

---

## License
MIT — see `LICENSE`

---

## Credits
Data: Spotify 2024 dataset from Kaggle 
Visualization: Tableau  
Data prep: Python/pandas (Colab)

## Author
Sai Krishna
