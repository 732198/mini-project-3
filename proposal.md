# PROPOSAL.md
## Mini Project #3 - Interactive Web Tool

---

**What I'm building:**
A personal health dashboard that connects to the WHOOP API and lets users
explore their recovery scores, sleep data, strain levels, and heart rate
trends in one place — with filtering, search, and visual charts.

---

**Who it's for / Why:**
Built for WHOOP members who want a cleaner, more focused way to explore
their own health data without digging through the official app. The goal
is to surface patterns and insights (like how sleep affects next-day
recovery) in a way that feels personal and easy to browse.

---

**Core features:**
1. Authenticate with WHOOP via OAuth 2.0 to pull real user data
2. Dashboard view showing today's recovery score, strain, and sleep performance
3. 30-day trend charts for HRV, resting heart rate, and recovery score
4. Sleep breakdown — stage durations (REM, deep, light) per night with
   a filterable date range
5. Workout log with sport labels, strain levels, and keyword search

---

**What I don't know yet:**
- How OAuth 2.0 works end-to-end and where to store the access token
  safely on the client side
- How to paginate through the WHOOP API responses since data comes back
  in chunks with a next_token cursor
- How to structure and cache fetched data so the app doesn't re-fetch
  everything on every interaction
- How to build the charts (leaning toward Chart.js) and connect them to
  live data so they update when the date filter changes