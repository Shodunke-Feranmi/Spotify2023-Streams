# Spotify 2023 Most Streamed Songs Analysis
 
A Power BI Project analyzing the most-streamed songs and artists on Spotify, covering five years of streaming trends (2019–2023), top tracks and artists, danceability, and platform distribution.
 
---
 
## 📌 Project Overview
 
This project analyzes a track-level Spotify dataset covering song streams, release year, artist, danceability, and platform/chart presence (Apple, Deezer, Shazam charts and playlists). The dashboard is fully interactive, filterable by **Platform** and **Year**.
 
| Metric | Value |
|---|---|
| Years Covered | 2019–2023 |
| Total Streams (5 years) | 895bn |
| Top 10 Artists' Combined Streams | 308bn |
| Top 10 Songs' Combined Streams | 143.2bn |
 
## 🎯 Business Problem
 
A music platform or label wants to understand what actually drives streaming success: which artists and songs dominate, whether streaming demand is seasonal, what song characteristics (like danceability) correlate with popularity, and where listening happens across platforms, so marketing and playlist strategy can be data-driven rather than guesswork.
 
## 📊 Project Objectives
 
- Track total streams year over year from 2019 to 2023
- Identify the top artists and top songs by total streams
- Analyze average streams by month to check for seasonal demand
- Compare songs by danceability percentage
- Break down stream volume by platform (Apple, Deezer, Shazam charts and playlists)
 
## 🛠️ Tools & Technologies
 
- **Power BI**
  - Data modeling
  - Line, bar, column, and donut charts
  - Interactive slicers 

## 📈 Key Findings
 
- **2022 was the peak streaming year** in the dataset, at **288bn streams**, up 22.6% from 2021 (235bn). **2023 shows only 78bn**, but this reflects a partial year of data rather than an actual decline — the dataset does not cover a full 2023.
- **2020 was the low point** (138bn), down 11.5% from 2019 (156bn), consistent with reduced new-release activity during that period, before streaming rebounded sharply in 2021 (+70.3%).
- **Ed Sheeran (56bn) and The Weeknd (54bn) lead all artists**, well ahead of Harry Styles (40bn) and Taylor Swift (32bn). The top 10 artists combine for **308bn streams**.
- **"Blinding Lights" is the most-streamed individual song** (18.5bn), followed by "Shape of You" (17.8bn) and "Someone You Loved" (14.4bn).
- **Average streams by month decline steadily from September (0.97bn) down to April (0.48bn)** — roughly a 2x difference between the highest and lowest month.
- **Streams are split exactly evenly across all 5 platform categories** (Apple Charts, Apple Playlists, Deezer Charts, Deezer Playlists, Shazam Charts) at 332bn / 20% each.
## 💡 Business Insights
 
1. **2022 is the true benchmark year, not 2023.** Since 2023's 78bn figure is a partial-year total, comparing it directly to full years like 2022 understates the real trend. Any reporting on this dashboard should clearly label 2023 as "year to date" to avoid the misleading impression that streaming collapsed.
2. **A small group of artists and songs dominate total volume.** The top 10 artists alone account for 308bn streams, and 2 artists (Ed Sheeran, The Weeknd) contribute nearly 110bn of that on their own. Marketing and licensing decisions built around "the top artist" rather than "the average artist" will capture most of the platform's value.
3. **Streaming demand is not flat across the year.** The near 2x gap between the strongest month (September, 0.97bn average) and the weakest (April, 0.48bn) suggests real seasonal listening patterns worth planning content releases and promotions around, though this should be confirmed against actual calendar-ordered data (see note below).
## ⚠️ Data Notes
 
- **Platform breakdown looks miscalculated.** All 5 platform categories show identical values (332bn / 20% each), which is extremely unlikely for real streaming distribution across Apple, Deezer, and Shazam. This pattern typically happens when a measure sums total streams once per row instead of per platform, effectively counting the same total 5 times. Worth checking the DAX measure or the underlying join before presenting this chart.
- **Danceability chart values exceed a normal 0–100% scale** (up to 705), so this chart is likely summing danceability across duplicate rows or multiple chart appearances of the same song, rather than showing a true per-song percentage. This should be corrected (e.g., using an average) before presenting it as "Highest Danceability % Songs."
- **The monthly streams chart is not sorted chronologically** — the axis runs Sep → Jan → Oct → Nov → Aug → Jul → Jun → May → Mar → Dec → Feb → Apr, sorted by value rather than calendar order, which makes the line look like a steady decline even though the months themselves aren't in sequence. It's worth re-sorting this by actual month order to confirm whether a real seasonal trend exists.
## 📸 Dashboard
 
![Spotify 2023 Streams Dashboard](images/Spotify2023streams.png)
 
## 📚 Skills Demonstrated
 
- Power BI data modeling
- Interactive dashboard design with slicers
- Time-series and seasonal trend analysis
- Ranking and top-N visualizations
- Critical data validation (catching measure and sorting errors before presenting)
## 👤 Author
 
**[Shodunke Feranmi]**
  [GitHub](https://github.com/Shodunke-Feranmi)
