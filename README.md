# Expense Tracker 💰

> A modern, full-stack web application to track, manage, and analyze your personal finances.



## 📖 Overview

Managing personal finances shouldn't be complicated. This Expense Tracker is a comprehensive, full-stack application designed to simplify how you monitor your spending. Built with a robust React frontend and a secure Express/PostgreSQL backend, it offers an intuitive interface for logging transactions, visualizing financial trends, and securely managing your account data. 

## ✨ Features

* **Secure Authentication:** Local strategy authentication utilizing `passport.js` and secure session management.
* **Intuitive Dashboard:** A responsive, interactive user interface built with React, Radix UI components, and Tailwind CSS.
* **Expense Management:** Easily add, edit, categorize, and delete financial transactions.
* **Data Visualization:** Interactive charts and graphs powered by `recharts` to visualize spending habits over time.
* **Type-Safe Database Operations:** Powered by Drizzle ORM and PostgreSQL for highly reliable and strongly typed data queries.
* **Real-time Form Validation:** Schema-based form validation using `zod` and `react-hook-form`.

## 🛠️ Tech Stack

| Category | Technologies |
| :--- | :--- |
| **Frontend** | React 18, Vite, Wouter (Routing), Tailwind CSS, Framer Motion |
| **UI Components** | Radix UI, Lucide React, Embla Carousel |
| **State Management** | React Query (`@tanstack/react-query`), React Hook Form |
| **Backend** | Node.js, Express.js, TypeScript |
| **Database & ORM** | PostgreSQL (`pg`), Drizzle ORM, Drizzle Kit |
| **Authentication** | Passport.js, Express Session, `connect-pg-simple` |
| **Validation** | Zod, `drizzle-zod` |

## 🏗️ Architecture

The application follows a modern client-server architecture, utilizing a RESTful API to communicate between the React frontend and the Express backend. 

```mermaid
graph TD
    Client[React Frontend Vite] -->|REST API calls| Server[Express.js Backend]
    Server -->|Auth / Sessions| Passport[Passport.js & Session Store]
    Server -->|SQL Queries| ORM[Drizzle ORM]
    ORM -->|Read/Write| DB[(PostgreSQL Database)]
📁 Project Structure
Based on the environment configuration, the project is structured to separate the core application logic:

Plaintext
├── pte-main/
│   ├── server/           # Express backend logic, API routes, and controllers
│   │   └── index.ts      # Main server entry point
│   ├── client/           # React frontend source code (components, pages, hooks)
│   ├── script/           # Build and utility scripts
│   └── drizzle.config.ts # Drizzle ORM configuration
├── .gitignore
├── package.json          # Project dependencies and npm scripts
└── README.md
🚀 Installation
Prerequisites:

Node.js (v18 or higher recommended)

PostgreSQL database instance

Clone the repository:

Bash
git clone [https://github.com/YOUR_USERNAME/Expense-tracker-MERN-.git](https://github.com/YOUR_USERNAME/Expense-tracker-MERN-.git)
cd Expense-tracker-MERN-
Install dependencies:

Bash
npm install
Database Setup:
Ensure your PostgreSQL server is running. Push the database schema using Drizzle:

Bash
npm run db:push
💻 Usage
Development Mode:
To run both the backend server and frontend client in development mode with hot-reloading:

Bash
npm run dev
Production Build:
To build the application for production:

Bash
npm run build
⚙️ Configuration
Create a .env file in the root directory and configure the following required environment variables:

Code snippet
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
DATABASE_URL=postgresql://username:password@localhost:5432/expense_tracker_db

# Session/Auth Configuration
SESSION_SECRET=your_super_secret_session_key
🔌 API & Modules
Authentication Module: Handles user registration, login, and session persistence using Passport.js.

Transactions API: REST endpoints (GET, POST, PUT, DELETE) to manage user expenses and incomes.

User API: Endpoints to retrieve and update user profile information.

Drizzle Schema: Defines the strongly typed database schema for Users and Transactions tables.


🤝 Contributing
Contributions, issues, and feature requests are welcome!

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

🗺️ Roadmap
[ ] Add support for multiple currencies and exchange rates.

[ ] Implement recurring transactions and subscription tracking.

[ ] Introduce an option to export data to CSV/PDF.

[ ] Add dark mode toggle (foundation already laid with next-themes).

📄 License
This project is licensed under the MIT License - see the https://www.google.com/search?q=LICENSE file for details.
