# Spotify Top 50 World — Power BI Dashboard

An interactive Power BI dashboard analyzing the **Spotify Global Top 50** chart from **May 2023 to November 2024**, covering 27,800 chart entries across 342 artists and 789 songs — built with a custom Spotify-themed dark UI.

---

## Dashboard Preview

![Spotify Dashboard Overview](https://github.com/user-attachments/assets/44d07d5a-dee4-433a-894e-ede9d7eb3b7e))

> *Open `Spotify.pbix` in Power BI Desktop to explore all 4 interactive pages.*

---

## Pages

The dashboard is organized into **4 pages**, accessible via the top navigation bar:

| Page | Description |
|---|---|
| **Home** | Landing/intro page |
| **Overview** | High-level KPIs, charts, and trends |
| **Artists** | Artist-focused breakdown and rankings |
| **Songs** | Song-level detail and exploration |

---

## Overview Page — Visuals

### Left Panel — Songs by Artist
A scrollable list of artists with album artwork thumbnails and their associated songs, making it easy to browse the dataset visually.

### KPI Cards
| Metric | Value |
|---|---|
| Count of Artists | 342 |
| Distinct Songs | 789 |
| Avg Duration | 3.28 minutes |
| Avg Popularity | 90 |

### Music Player Visual
A custom-designed music player widget at the center of the Overview page, displaying album art with playback-style navigation controls — styled to match the Spotify app experience.

### Donut Charts
| Chart | Insight |
|---|---|
| **Song by Album Type** | Album 66.9% · Single 32.02% |
| **Explicit vs Non-Explicit** | Non-Explicit 17K · Explicit 11K |
| **Song by Year** | 2023 51.43% · 2024 48.57% |
| **Avg Popularity by Album Type** | Singles 35.82% · Albums 34.44% · Other 29.74% |

### Bar Charts
- **Songs by Artist** — Top artists ranked by number of charting songs (Taylor Swift leads with 85)
- **Top Songs by Artist** — Most-streamed songs ranked by total plays (e.g., *I Wanna...* at 51K)

### Time Series Charts
- **Avg Popularity by Month** — Line chart with **Month / Quarter** toggle showing popularity trends across the year (Jan–Dec)
- **Distinct Songs by Month** — Bar chart showing how many unique songs charted each month (peak: ~220 in September)

---

## Dataset

**File:** `spotify-top-50-world.csv`

| Column | Description |
|---|---|
| `date` | Chart snapshot date |
| `position` | Chart position (1–50) |
| `song` | Track name |
| `artist` | Artist name |
| `popularity` | Spotify popularity score (0–100) |
| `duration_ms` | Track duration in milliseconds |
| `album_type` | Album, single, or EP |
| `total_tracks` | Number of tracks in the release |
| `release_date` | Original release date of the track |
| `is_explicit` | Whether the track contains explicit content |
| `album_cover_url` | Spotify CDN URL for the album artwork |

**Stats at a glance:**
- **27,800** chart entries
- **789** unique songs
- **342** unique artists
- **Date range:** May 18, 2023 – November 27, 2024

---

## Design

- Dark theme matching Spotify's native color palette (`#121212` background, Spotify green `#1DB954`)
- Custom icon set: music player controls, microphone, trending, musical note, and Spotify logo
- Custom background images per page
- Scrollable artist sidebar with embedded album art

---

## Files

```
Spotify/
├── Spotify.pbix                     # Power BI dashboard (all 4 pages)
├── spotify-top-50-world.csv         # Source dataset (27,800 rows)
├── Backgrounds-*/                   # Background images for each dashboard page
├── drive-download-*/                # Custom icon assets (player controls, logos)
└── README.md
```

---

## Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)

### Steps

1. Clone or download this repository
2. Open **Power BI Desktop**
3. Open `Spotify.pbix`
4. If prompted to refresh data, point it to the included `spotify-top-50-world.csv`
5. Use the top navigation bar to switch between pages: **Home → Overview → Artists → Songs**

---

## Tools Used

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard design and data visualization |
| DAX | Calculated measures and KPIs |
| Spotify Web API | Original data source |
| CSV | Data storage format |

---

## 📬 Connect

Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/yash-shah-97a595175/) or raise an issue if you have suggestions or questions!
