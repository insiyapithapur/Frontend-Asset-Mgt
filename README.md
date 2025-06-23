
# Final Asset Management v1 🛠️

A modern, **React 18 + Material-UI 5** dashboard that helps organisations keep track of their physical and digital assets in one place.  
The project is built on the [Minimal UI Kit] template and deployed on Vercel for instant preview.

<p align="center">
  <a href="https://assetmgt-kirtans-projects-5b9e01d8.vercel.app" target="_blank">
    <img alt="Live Demo" src="https://img.shields.io/badge/Live-Demo-green?logo=vercel&logoColor=white">
  </a>
  <img alt="Node" src="https://img.shields.io/badge/Node-16%20%7C%2018-blue?logo=node.js">
  <img alt="License" src="https://img.shields.io/badge/License-Contact%20Repo%20Owner-lightgrey">
</p>

---

## ✨ Key Features
| Domain | Highlights |
| ------ | ---------- |
| **Inventory** | CRUD for asset categories, models & locations |
| **Dashboards** | Real-time charts via **ApexCharts** & **TanStack React-Query** |
| **Scheduling** | Asset bookings & maintenance timeline with **FullCalendar** |
| **Mapping** | Geo-plot assets on **Mapbox GL** interactive maps |
| **Docs & Export** | One-click PDF reports using **@react-pdf/renderer** |
| **Auth** | Pluggable providers – **Auth0**, **Firebase** or **AWS Amplify-Auth** |
| **UX** | Material-UI 5 theme, drag-and-drop (Hello Pangea DnD), rich text, data grid |

---

## 📂 Project Structure
```
final_asset_mgt_v1
├── build/          # Production build (auto-generated)
├── public/         # Static assets & index.html
├── src/            # React source code
│   ├── components/ …
│   ├── hooks/ …
│   └── routes/ …
├── README.md
├── package.json
└── yarn.lock / package-lock.json
```

---

## 🚀 Quick Start

### Prerequisites
* **Node 16 or 18**  
* **Yarn (v1+)** – recommended, but `npm` works too.

```bash
# 1. Clone the repo
git clone https://github.com/kirtanlab/final_asset_mgt_v1.git
cd final_asset_mgt_v1

# 2. Install dependencies
yarn install        # or: npm i --legacy-peer-deps

# 3. Run the dev server
yarn start          # or: npm start
```

### Common Scripts
| Script            | What it does |
| ----------------- | ------------ |
| `yarn start`      | Launch dev server with hot reload |
| `yarn build`      | Production build to `/build` |
| `yarn lint`       | Run ESLint |
| `yarn lint:fix`   | ESLint + auto-fix |
| `yarn prettier`   | Prettier formatting |
| `yarn clear-all`  | Wipe caches & build artefacts |
| `yarn re-start`   | Full clean → reinstall → start |
| `yarn re-build`   | Full clean → reinstall → build |

---

## 📘 Enterprise Application Overview

This system is an enterprise asset management platform that focuses on the full life cycle of assets, including categories, classifications, types, locations, employees, and asset requests. It enhances transparency, simplifies maintenance, and improves compliance and security.

### 🏢 Business Overview
**Problem Areas and Solutions**  
Covers asset archive management, employee linkage, request approval flow, dashboard statistics, classification control.

**Target Users**  
- **Admins**: Full permissions
- **Employees**: Can request assets and view status
- **Approvers**: Maintain classification and approvals
- **Guests**: Limited access as per config

**Business Value**  
- Full life-cycle asset tracking  
- Role-based permissions  
- Scalable, location-aware deployment  
- Standardized operations and compliance

---

## 🏗️ Architecture Overview

### System Architecture
- **Frontend**: React SPA with Material-UI
- **Logic**: Components, hooks, and contexts
- **API Layer**: Axios-based connection to backend (not included)

### Technology Stack
- **React**, **Material UI**, **Axios**, **JWT**, **Mapbox**, **Chart.js**
- Backend not included but assumed Node.js 16/18
- Mock data lives in `src/_mock/`

### Module Highlights
- **Asset Requests**: Submit, approve, track
- **Metadata**: Categories, Types, Locations
- **Dashboard**: Chart-based analytics
- **Map**: Mapbox-powered geo views
- **Auth**: JWT via React context

---

## 🔐 Security & Access

- **JWT Auth**: In `src/auth/context/jwt`
- **Role Guards**: Access control in `src/auth/guard/`
- **Secure Pages**: 403/404/500 custom routes

---

## ⚙️ Deployment & Configuration

```bash
git clone https://github.com/kirtanlab/final_asset_mgt_v1
cd final_asset_mgt_v1
yarn install   # or npm install
yarn start     # or npm start
```

- No default `.env` – see `src/config-global.js` and `src/apis/Config.js`
- Mapbox token, API endpoints are manually configured

---

## 🧩 Additional Notes

- No tests found; manual/integration testing encouraged
- Asset modules in `src/pages/`, `src/components/`, `src/sections/`
- No backend/db structure – front-end only project
- CI/CD not yet configured
