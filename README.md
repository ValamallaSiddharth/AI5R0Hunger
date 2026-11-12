# AI5R0Hunger: Ending Hunger Sustainably with Artificial Intelligence

[![UN SDG](https://img.shields.io/badge/UN%20SDG-Goal%202%3A%20Zero%20Hunger-darkgreen.svg)](https://sdgs.un.org/goals/goal2)
[![Node.js](https://img.shields.io/badge/Node.js-Express%20API-339933.svg?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Database](https://img.shields.io/badge/Database-MongoDB-47A248.svg?logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Leaflet](https://img.shields.io/badge/Maps-Leaflet.js-199900.svg?logo=leaflet&logoColor=white)](https://leafletjs.com/)

---

## 📌 Overview

**AI5R0Hunger** is an initiative aimed at eliminating hunger, minimizing food waste, and optimizing food supply chains by combining **Artificial Intelligence (AI)** with the **5R Sustainability Framework** (*Refuse, Reduce, Reuse, Repurpose, Recycle*). 

Aligned directly with the United Nations' **Sustainable Development Goal 2 (Zero Hunger)**, the platform integrates predictive logistics, smart urban agriculture (including Green Roof monitoring), food rescue networks, and interactive geospatial mapping of hunger-affected regions.

---

## 🎯 The 5R Approach to Food Security

The project's foundational methodology centers on the 5R sustainability model:

| Principle | Meaning in AI5R0Hunger |
| :--- | :--- |
| **Refuse** | Reject overproduction and unnecessary farming/shipping through AI demand forecasting before waste begins. |
| **Reduce** | Minimize food supply chain inefficiencies, spoilage, and residential food waste using predictive analytics. |
| **Reuse** | Redirect edible surplus food from restaurants and retailers to communities and food banks; reuse rooftops for urban farming. |
| **Repurpose** | Convert food scraps into organic compost and animal feed; repurpose urban spaces for micro-agriculture. |
| **Recycle** | Employ eco-friendly packaging and recycle agricultural byproducts to return nutrients to the soil. |

---

## 🚀 Key Features & Solutions

1. **AI-Powered Food Distribution & Logistics**
   - Predictive analytics forecast food surplus and dispatch items rapidly to underserved communities before spoilage occurs.

2. **Smart Agriculture & Green Roof Monitoring**
   - AI and IoT sensors track plant health, soil moisture, and weather conditions on urban green rooftops, sending automated alerts to protect crops against extreme weather.

3. **Blockchain for Food Transparency**
   - Supply chain tracking to verify food freshness, fair distribution, and donor accountability.

4. **Interactive Hunger-Affected Region Mapping**
   - Built with **Leaflet.js** and OpenStreetMap tiles, visualizing global regions facing acute food shortages (e.g., South Sudan, Chad, Yemen, Somalia, Madagascar) to guide relief efforts.

5. **Food Rescue & Sustainable Consumption**
   - **Restaurant Surplus Rescue**: Direct surplus collection from cafes and dining establishments.
   - **Fireless Cooking**: Energy-efficient meal preparation utilizing heat retention insulation.
   - **Instant Meal Packets**: Quick-prep emergency meal solutions requiring only hot water.
   - **Waste-to-Food Conversion**: Bio-material recycling into nutritional food sources.

6. **Authentication & Community Engagement**
   - User sign-up and login portals supported by an Express/MongoDB backend, alongside community volunteer sign-up forms.

---

## 📂 Project Directory Structure

```text
AI5R0Hunger/
│
├── 0hunger.html                                                # Main landing page & navigation hub
├── About Us.html                                               # About page detailing the 5R framework
├── How It Works.html                                           # 5-step workflow breakdown of AI integration
├── Hunger-Affected.html                                        # Interactive Leaflet.js crisis location map
├── Our Mission.html                                            # Mission statement and core principles
├── Solutions.html                                              # Showcase of 8 sustainable food solutions
├── log.html                                                    # User login interface
├── sign.html                                                   # User sign-up interface
│
├── server.js                                                   # Node.js + Express + MongoDB backend API
│
├── AI5R0Hunger-Ending-Hunger-Sustainably-with-Artificial-Intelligence (1).pptx  # Project presentation deck
│
├── Imagesss/                                                   # Asset sub-folder
│   ├── AI5R0Hunger.jpg
│   ├── join.jpg
│   ├── Location.jpg.png
│   ├── logo.jpg
│   ├── our mission.jpg
│   ├── solutions.jpg
│   └── works.jpg
│
└── [Root Images]                                               # UI media assets
    ├── ai-.jpg, Ai.jpg, ai_greenroof.jpg, back.jpg, block.jpg,
    ├── Food Dis.jpg, food-quality.jpg, food.jpg, green roof.jpg,
    ├── fireless-cooking.jpg, Instant Meal Packets.jpg, real.jpg,
    ├── restaurant-surplus.png, smart.jpg, waste-to-food.jpg,
    └── DALL·E ... .webp
```

---

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3 (Responsive Flexbox, Poppins typography), JavaScript (ES6)
- **Mapping Library**: [Leaflet.js v1.7.1](https://leafletjs.com/) & OpenStreetMap
- **Backend**: [Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/) via [Mongoose ODM](https://mongoosejs.com/)
- **Middleware**: CORS, Body-Parser
- **Media / Design**: Custom & AI-generated illustrations (DALL-E)

---

## ⚡ Getting Started

### 1. Running the Frontend
The web pages are static and can be run in any modern web browser:
1. Open [`0hunger.html`](file:///c:/Users/V.Siddharth/OneDrive/Desktop/normal/AI5R0Hunger/0hunger.html) directly in your browser (e.g., Chrome, Edge, Firefox).
2. Alternatively, use a local development server such as VS Code's **Live Server** extension or `npx serve .` to serve the files locally.

### 2. Setting Up the Backend Server

#### Prerequisites
- [Node.js](https://nodejs.org/) (v14+ recommended)
- [MongoDB](https://www.mongodb.com/) running locally on default port `27017`

#### Installation Steps
1. In the project root directory, initialize a `package.json` (if not already present):
   ```bash
   npm init -y
   ```
2. Install the necessary dependencies:
   ```bash
   npm install express mongoose cors body-parser
   ```
3. Start the backend server:
   ```bash
   node server.js
   ```
4. The server will start and listen at:
   ```text
   http://localhost:3000
   ```

#### Backend Endpoints
- `POST /signup`: Registers a new user.
  - **Body (JSON)**:
    ```json
    {
      "name": "Jane Doe",
      "email": "jane@example.com",
      "password": "securepassword123"
    }
    ```
  - **Responses**:
    - `201 Created`: `{ "message": "User registered successfully!" }`
    - `500 Internal Server Error`: `{ "error": "Error registering user." }`

---

## 🔍 Recommended Improvements & Housekeeping

During project inspection, the following areas were noted for optimization:
- **Relative Navigation Links**: In [`0hunger.html`](file:///c:/Users/V.Siddharth/OneDrive/Desktop/normal/AI5R0Hunger/0hunger.html), internal links use absolute Windows file paths (e.g., `file:///C:/Users/.../About%20Us.html`). Changing these to relative paths (e.g., `./About Us.html`) will ensure the links work on any computer or web host.
- **Image Directory Consistency**: Several images are located in the root folder, while others are in `Imagesss/`. Standardizing all image sources to a single `images/` directory will improve maintainability.
- **Frontend-Backend Integration**: The registration form in [`sign.html`](file:///c:/Users/V.Siddharth/OneDrive/Desktop/normal/AI5R0Hunger/sign.html) can be connected to the `POST /signup` endpoint in [`server.js`](file:///c:/Users/V.Siddharth/OneDrive/Desktop/normal/AI5R0Hunger/server.js) via a JavaScript `fetch()` submission handler.
- **`package.json`**: Adding a committed `package.json` will allow collaborators to run `npm install` without manual setup.

---

## 📄 License & Credits

- **Initiative**: AI5R0Hunger
- **Target Goal**: [United Nations SDG 2 — Zero Hunger](https://sdgs.un.org/goals/goal2)
- **Year**: 2025–2026
