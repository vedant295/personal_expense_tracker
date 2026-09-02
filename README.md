# 💰 Personal Expense Tracker

A simple, centralized web/mobile application to record, categorize, and analyze your daily expenses — helping you understand your spending patterns, set realistic budgets, and avoid overspending.

<p align="left">
  <img alt="status" src="https://img.shields.io/badge/status-in%20development-yellow">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-blue">
  <img alt="node" src="https://img.shields.io/badge/node-%3E%3D18-green">
</p>

---

## 📖 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Architecture](#-project-architecture)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Running the App](#running-the-app)
- [Folder Structure](#-folder-structure)
- [API Overview](#-api-overview)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 📌 About the Project

Most people struggle to track where their money goes each month — expenses are scattered across cash, bank accounts, credit cards, and UPI wallets, making it hard to get a consolidated view of spending.

**Personal Expense Tracker** solves this by giving users a single place to:

- Log every expense with amount, category, date, and payment mode
- Set monthly budgets per category and get alerted before overspending
- Visualize spending trends through charts and summaries
- Export data for offline record-keeping

---

## ✨ Features

- 🔐 **Secure Authentication** — Register, log in, and manage your profile
- ➕ **Expense Management** — Add, edit, and delete expense entries
- 🏷️ **Custom Categories** — Use default categories or create your own
- 🎯 **Budgeting** — Set monthly budgets per category with 80%/100% threshold alerts
- 📊 **Reports & Analytics** — Pie charts, bar charts, and trend graphs of your spending
- 🔍 **Search & Filter** — Find expenses by date range, category, or payment mode
- 📤 **Data Export** — Download your records as PDF or CSV
- 📱 **Responsive UI** — Works on both desktop and mobile screens

---

## 🛠️ Tech Stack

> The stack below reflects the recommended setup for this project. Swap in whatever the actual implementation uses.

| Layer | Technology |
|---|---|
| Frontend | React.js (or HTML/CSS/JavaScript) |
| Backend | Node.js + Express.js |
| Database | MongoDB (or MySQL / PostgreSQL / SQLite) |
| Authentication | JWT + bcrypt |
| Charts | Chart.js / Recharts |
| Deployment | Render / Vercel / Netlify |

---

## 🏗️ Project Architecture

```
Client (Web / Mobile)
        │
        ▼
   REST API (Express)
        │
        ▼
     Database
```

The application follows a client-server architecture. The client communicates with a backend REST API that handles authentication, expense records, budgets, and report generation, backed by a database.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) (local instance or a free [Atlas](https://www.mongodb.com/atlas) cluster) — or your chosen database

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/personal-expense-tracker.git
   cd personal-expense-tracker
   ```

2. **Install backend dependencies**

   ```bash
   cd server
   npm install
   ```

3. **Install frontend dependencies**

   ```bash
   cd ../client
   npm install
   ```

### Environment Variables

Create a `.env` file inside the `server` folder with the following variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

### Running the App

**Start the backend server:**

```bash
cd server
npm run dev
```

**Start the frontend (in a separate terminal):**

```bash
cd client
npm start
```

The app should now be running at `http://localhost:3000` (frontend) and `http://localhost:5000` (backend API).

---

## 📁 Folder Structure

```
personal-expense-tracker/
├── client/                 # Frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # App pages/screens
│   │   ├── services/       # API calls
│   │   └── App.js
│   └── package.json
├── server/                 # Backend application
│   ├── controllers/        # Route logic
│   ├── models/             # Database schemas
│   ├── routes/             # API route definitions
│   ├── middleware/         # Auth & error handling
│   └── server.js
├── docs/                   # Project documentation (SRS, use case diagrams, etc.)
├── .env.example
├── README.md
└── LICENSE
```

---

## 🔌 API Overview

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate a user |
| GET | `/api/expenses` | Get all expenses for the logged-in user |
| POST | `/api/expenses` | Add a new expense |
| PUT | `/api/expenses/:id` | Update an existing expense |
| DELETE | `/api/expenses/:id` | Delete an expense |
| GET | `/api/categories` | Get all categories |
| POST | `/api/budgets` | Set a monthly budget for a category |
| GET | `/api/reports/summary` | Get category-wise and trend summary |
| GET | `/api/export` | Export expenses as PDF/CSV |

> Full API documentation can be added in `docs/API.md`.

---

## 🖼️ Screenshots

| Dashboard | Add Expense | Reports |
|---|---|---|
| _add screenshot_ | _add screenshot_ | _add screenshot_ |

---

## 🗺️ Roadmap

- [ ] Bank/UPI auto-transaction import
- [ ] Multi-currency support
- [ ] Shared/family budgeting
- [ ] Recurring expense reminders
- [ ] Dark mode

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

---


