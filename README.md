# 🌸 Shelfy — Google Books API Data Visualization

> A pastel‑themed, React‑based dashboard turning Google Books data into interactive, human‑centered insights using Chart.js and Recharts.

<p align="center">
  <img src="./assets/shelfy_preview.png" alt="Shelfy preview" width="820">
</p>

---

## Table of Contents
- [Overview](#overview)
- [Live Demo & Repository](#live-demo--repository)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage Guide](#usage-guide)
- [Data Model & Sources](#data-model--sources)
- [Screenshots](#screenshots)
- [Development Process](#development-process)
- [Testing](#testing)
- [Limitations](#limitations)
- [Roadmap / Future Improvements](#roadmap--future-improvements)
- [Acknowledgements](#acknowledgements)
- [Author](#author)
- [License](#license)

---

## 🌿 Overview
**Shelfy** is an interactive data visualization app that connects with the **Google Books API** to transform book metadata into meaningful, visual stories.  
It’s built with **React** and designed using a **pastel‑inspired, minimal aesthetic** that emphasizes clarity, usability, and emotion in data interpretation.  

Users can explore and compare books by genre, rating, price proxy, and publication recency through charts, filters, and modular interactions.

---

## 🔗 Live Demo & Repository
**Repository:** [https://github.com/AngievR05/shelfy_react_app.git](https://github.com/AngievR05/shelfy_react_app.git)

> For grading or review, clone this repo and run it locally as described below.

---

## 💫 Features
- 🔍 **Search & Discover** — Fetch live book data using the Google Books API.
- 🧠 **Interactive Charts** — Bar, Pie, and Radar charts powered by Chart.js & Recharts.
- 🎨 **Pastel UI** — Soft, accessible color palette optimized for readability.
- 🧭 **Genre Filtering** — Easily toggle between genres to update your dataset.
- 📊 **Comparison Mode** — Compare two books visually across metrics like rating, pages, and recency.
- 💬 **Book Modal** — Displays authors, ratings, page count, and cover in a clean overlay.
- 🕒 **Timeline Visualization** — See when books were published relative to each other.
- 📱 **Responsive Design** — Optimized for all screen sizes and devices.

---

## 🧩 Architecture
```
shelfy/
├── public/
│   └── index.html
├── src/
│   ├── assets/                # image assets for README/UI
│   ├── components/            # reusable UI building blocks
│   │   ├── BookList.js
│   │   ├── BookModal.js
│   │   ├── ChartSection.js
│   │   ├── CombinedDataChart.js
│   │   ├── GenreSelector.js
│   │   ├── DashboardCard.js
│   │   ├── Footer.js
│   │   ├── PriceChart.js
│   │   ├── RatingsChart.js
│   │   └── Header.js
│   ├── pages/
│   │   ├── Dashboard.js
│   │   ├── Comparison.js
│   │   ├── Timeline.js
│   │   └── NotFound.js
│   ├── css/
│   ├── App.js
│   ├── index.js
│   └── reportWebVitals.js
└── package.json
```

---

## 🧠 Tech Stack
**Frontend:** React, Chart.js, Recharts, CSS3  
**API:** Google Books API  
**State Management:** React Hooks (`useState`, `useEffect`)  
**Tooling:** Create React App  
**Styling:** Modular CSS (lightweight pastel theme)

<div align="center">
  
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=000)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chartdotjs&logoColor=fff)
![Recharts](https://img.shields.io/badge/Recharts-22CEB1)
![Google Books](https://img.shields.io/badge/Google%20Books%20API-4285F4?logo=google&logoColor=fff)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=fff)

</div>

---

## 🧰 Getting Started

### Prerequisites
- Node.js (LTS version recommended)
- npm

### Installation
```bash
git clone https://github.com/AngievR05/shelfy_react_app.git
cd shelfy_react_app
npm install
```

### Environment Variables
To use your own Google Books API key, create a `.env` file:
```
REACT_APP_GOOGLE_BOOKS_API_KEY=your_key_here
```

### Run Locally
```bash
npm start
```
The app will open at **http://localhost:3000**

---

## 🧭 Usage Guide
1. Enter a keyword or book title to search.
2. Select a genre from the toggle list.
3. Click on a book to open its detailed modal.
4. Switch to **Comparison Mode** to compare books visually.
5. View **Timeline** for historical publishing trends.

---

## 📈 Data Model & Sources
**Source:** Google Books API `/volumes` endpoint  
**Mapped Fields:** `title`, `authors`, `averageRating`, `pageCount`, `publishedDate`, and `imageLinks.thumbnail`  
**Normalization:** Missing data is gracefully handled (e.g., "No Rating" labels).

---

## 📸 Screenshots

<p align="center">
  <img src="./assets/dashboard.png" alt="Dashboard" width="820"><br/>
  <em>Dashboard — search, genre filtering, and featured books.</em>
</p>

<p align="center">
  <img src="./assets/comparison.png" alt="Comparison View" width="820"><br/>
  <em>Comparison View — visual radar and bar charts of two books.</em>
</p>

<p align="center">
  <img src="./assets/modal.png" alt="Book Modal" width="820"><br/>
  <em>Book Modal — detailed data including rating and description.</em>
</p>

---

## 🧩 Development Process

### Design Decisions
- Emphasized **data storytelling** with a calm, user‑friendly visual tone.  
- Chose **pastel palette** to balance readability and emotional engagement.  
- Component modularity for scalability and reusability.

### State Management
- Local and lifted state via `useState` and `useEffect`.
- Derived data structures feed chart components cleanly.

### Accessibility
- Proper aria‑labels, semantic headings, and tab navigation.
- Tested for contrast compliance (WCAG AA).

### Performance
- Debounced search requests.
- Lazy‑loading charts when inactive.
- Minimal re‑renders using memoized props.

---

## 🧪 Testing
- Manual exploration for search, chart rendering, and filters.  
- Edge‑case testing with missing ratings or malformed API responses.

---

## ⚠️ Limitations
- Some API responses lack price or rating data.  
- API rate limits may slow down consecutive searches.  

---

## 🚀 Roadmap / Future Improvements
- Add **local storage** for saving previous searches.  
- Implement **weighted scoring algorithm** for comparing books.  
- Introduce **dark mode** toggle.  
- Add **chart export** and print‑friendly views.  
- Expand into **author insights** using additional endpoints.

---

## 🌼 Acknowledgements
- Google Books API  
- Chart.js & Recharts community  
- Open Window DV200 faculty for project brief and guidance  

---

## 👩‍💻 Author
**Angie Christine van Rooyen**  
📧 241077@virtualwindow.co.za  
🔗 [LinkedIn](https://www.linkedin.com/in/angie-van-rooyen-7008712a7/)

---

## 📜 License
Licensed under the **MIT License** — feel free to fork, improve, or build upon this project.
