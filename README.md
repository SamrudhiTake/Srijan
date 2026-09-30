# 🌟 SRIJAN 2026 — Official Tech Fest Platform

<p align="center">
  <img src="frontend/src/assets/srijan-logo.jpg" alt="Srijan 2026 Logo" width="180" style="border-radius: 20px; box-shadow: 0 10px 30px rgba(245, 158, 11, 0.2);" />
</p>

<p align="center">
  <strong>TOGETHER, WE CREATE</strong><br>
  <em>A Technical Fest Where Ideas Turn Into Innovation</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Edition-2026-amber?style=for-the-badge" alt="Edition 2026" />
  <img src="https://img.shields.io/badge/Stack-MERN-blue?style=for-the-badge" alt="MERN Stack" />
  <img src="https://img.shields.io/badge/Frontend-React%20%2B%20Vite%20%2B%20Tailwind-61DAFB?style=for-the-badge" alt="React Vite" />
  <img src="https://img.shields.io/badge/Backend-Node.js%20%2B%20Express%20%2B%20MongoDB-green?style=for-the-badge" alt="Node Express Mongo" />
</p>

---

## 📖 About Srijan

**SRIJAN** is the annual flagship technical festival bringing together students, builders, innovators, and thinkers across engineering institutions. It provides a competitive platform for students to test their practical skills, problem-solving abilities, and engineering creativity.

### 🏛️ The Four Pillars of Srijan
1. **💡 INNOVATE (Ideation):** Challenge conventional approaches and spark breakthrough concepts for real-world technical problems.
2. **🛠️ BUILD (Engineering):** Transform ideas into functional prototypes through focused engineering, coding, and collaborative development.
3. **🏆 COMPETE (Excellence):** Test your skills against collegiate minds in structured technical challenges and peer review.
4. **✨ CREATE (Impact):** Bring your vision to life under the guiding ethos: *Together, we create.*

---

## 🏆 Flagship Events Directory

| No. | Event Name | Category | Participation | Team Size | Code |
|:---:|:---|:---|:---:|:---:|:---:|
| **01** | **Hackathon** | Technical Competition | Team | 2–4 Members | `HACK` |
| **02** | **KBC Quiz** | Technical Quiz | Individual | 1 Member | `KBC` |
| **03** | **PCB Designing** | Technical Competition | Individual | 1 Member | `PCB` |
| **04** | **CAD Modeling** | Technical Competition | Individual | 1 Member | `CAD` |
| **05** | **Bridge Making** | Engineering Challenge | Individual | 1 Member | `BRG` |
| **06** | **Circuit Making** | Electronics Challenge | Individual | 1 Member | `CIRCUIT` |

---

## 📂 Project Architecture

The project is cleanly decoupled into two standalone applications: **`frontend/`** and **`backend/`**.

```
Srijan/
├── 🌐 frontend/                     # Client Web Application
│   ├── public/                      # Static assets & downloadable PDF brochures
│   │   └── brochures/               # Event PDF rulebooks (event-1.pdf to event-6.pdf)
│   ├── src/
│   │   ├── assets/                  # Logos, badges, and brand images
│   │   ├── components/              # Reusable React UI Components
│   │   │   ├── Navbar.jsx           # Responsive glassmorphism navigation
│   │   │   ├── Footer.jsx           # Brand footer with social links & event directory
│   │   │   ├── Hero.jsx             # Animated landing hero section
│   │   │   ├── StarfieldCanvas.jsx  # Interactive background canvas particle system
│   │   │   ├── EventCard.jsx        # Glassmorphic event display card
│   │   │   ├── EventGrid.jsx        # Filterable events grid
│   │   │   ├── EventDetails.jsx     # Full event specifications, schedule & rules
│   │   │   ├── RegistrationForm.jsx # Unified form controller (Solo & Team modes)
│   │   │   ├── IndividualRegistrationForm.jsx # Solo participant form with validation
│   │   │   ├── TeamRegistrationForm.jsx       # Dynamic multi-member team form
│   │   │   ├── RegistrationSuccess.jsx        # Printable confirmation receipt
│   │   │   └── BrochureModal.jsx    # PDF preview modal
│   │   ├── pages/                   # Application Pages
│   │   │   ├── Home.jsx             # Landing page
│   │   │   ├── EventsPage.jsx       # Complete event directory
│   │   │   ├── EventDetailsPage.jsx # Dedicated event overview
│   │   │   ├── Registration.jsx     # Registration gateway
│   │   │   ├── AboutPage.jsx        # About Srijan & college festival info
│   │   │   └── NotFoundPage.jsx     # Custom 404 page
│   │   ├── services/
│   │   │   └── api.js               # Centralized REST API client
│   │   ├── data/
│   │   │   └── events.js            # Initial events schema & festival metadata
│   │   ├── App.jsx                  # Main application routing
│   │   └── main.jsx                 # Vite application entry point
│   ├── vite.config.js               # Dev server & reverse proxy to backend (Port 9000)
│   ├── tailwind.config.js           # Custom Srijan dark theme color palette
│   ├── package.json                 # Frontend dependencies & scripts
│   └── .gitignore
│
├── ⚙️ backend/                      # REST API Server
│   ├── config/
│   │   └── db.js                    # MongoDB Mongoose connection handler
│   ├── models/
│   │   ├── Registration.js          # Indexed registration schema + ID generator
│   │   ├── Event.js                 # Event details schema with capacity counters
│   │   └── Contact.js               # Inquiries & messages schema
│   ├── controllers/
│   │   ├── registrationController.js# Registration, search, stats & CSV export logic
│   │   ├── eventController.js       # Event listings & single event lookup
│   │   └── contactController.js     # Contact submission handler
│   ├── routes/
│   │   ├── registrationRoutes.js    # /api/registrations endpoints
│   │   ├── eventRoutes.js           # /api/events endpoints
│   │   ├── contactRoutes.js         # /api/contact endpoint
│   │   └── healthRoutes.js          # /api/health diagnostic endpoint
│   ├── seeds/
│   │   ├── eventsData.js            # Seed data for all 6 Srijan events
│   │   └── seedEvents.js            # Database seeder script (`npm run seed`)
│   ├── server.js                    # Express application entry point
│   ├── .env                         # Server environment configuration
│   ├── .env.example                 # Example environment variables template
│   ├── package.json                 # Backend dependencies & scripts
│   └── .gitignore
│
├── 📄 README.md                     # Main project documentation
├── 🛡️ .gitignore                   # Master workspace gitignore
└── 📦 package.json                  # Root workspace script runner
```

---

## ⚡ Tech Stack

### Frontend
- **Framework:** [React 18](https://react.dev/)
- **Build Tool:** [Vite 5](https://vitejs.dev/)
- **Styling:** [Tailwind CSS 3](https://tailwindcss.com/) (Custom void/space theme, glowing gradients)
- **Icons:** [Lucide React](https://lucide.dev/)
- **Routing:** [React Router DOM 6](https://reactrouter.com/)
- **Graphics:** HTML5 Canvas Interactive Starfield Simulation

### Backend
- **Runtime:** [Node.js](https://nodejs.org/) (ES Modules)
- **Framework:** [Express.js 4](https://expressjs.com/)
- **Database:** [MongoDB](https://www.mongodb.com/) via [Mongoose 8](https://mongoosejs.com/)
- **Utilities:** CORS, Morgan (HTTP request logger), Dotenv, Nodemon

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v18 or higher recommended)
- **MongoDB** (Local instance or [MongoDB Atlas](https://www.mongodb.com/atlas) Cloud Cluster)
- **npm** or **yarn**

---

### Step 1: Clone and Setup Workspace

```bash
git clone <your-repository-url>
cd Srijan
```

---

### Step 2: Setup the Backend

1. Navigate to the `backend` directory and install dependencies:
   ```bash
   cd backend
   npm install
   ```

2. Configure environment variables:
   - Copy `.env.example` to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Set your MongoDB connection string in `backend/.env`:
     ```env
     PORT=9000
     NODE_ENV=development
     MONGODB_URI=mongodb://localhost:27017/srijan
     # Or use MongoDB Atlas:
     # MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/srijan?retryWrites=true&w=majority
     CLIENT_URL=http://localhost:3000
     ```

3. **(Optional)** Seed the 6 Srijan events into MongoDB:
   ```bash
   npm run seed
   ```

4. Start the backend development server:
   ```bash
   npm run dev
   ```
   > Server will start at: `http://localhost:9000`

---

### Step 3: Setup the Frontend

1. In a new terminal, navigate to the `frontend` directory:
   ```bash
   cd frontend
   npm install
   ```

2. Start the Vite development server:
   ```bash
   npm run dev
   ```
   > Application will launch at: `http://localhost:3000`

---

## 🛠️ Root Workspace Scripts

From the root `Srijan/` directory, you can also run:

| Command | Action |
|---|---|
| `npm run dev:frontend` | Starts the React frontend on `http://localhost:3000` |
| `npm run dev:backend` | Starts the Express server on `http://localhost:9000` with hot-reload |
| `npm run seed:backend` | Seeds all 6 Srijan events into the MongoDB database |
| `npm run build:frontend` | Compiles the production-ready frontend bundle into `frontend/dist` |
| `npm run install:all` | Installs dependencies for both frontend and backend |

---

## 🔌 API Endpoints Reference

### 1. Events API
- `GET /api/events` — Retrieve all Srijan events
- `GET /api/events/:eventId` — Retrieve details for a specific event (e.g. `event-1` or `HACK`)

### 2. Registrations API
- `POST /api/registrations` — Submit Individual or Team registration
- `GET /api/registrations/:id` — Lookup registration details by Registration ID (e.g. `SRJ-HACK-002250`)
- `GET /api/registrations` — Search and filter registrations:
  - `?q={keyword}` — Universal full-text search (Name, Email, Phone, College, Team Name, Registration ID)
  - `?eventId=event-1` — Filter by event
  - `?type=team` — Filter by participation type (`individual` / `team`)
  - `?college=GCOEA` — Filter by college name
  - `?page=1&limit=25` — Pagination support

### 3. Fest Analytics & Reports
- `GET /api/registrations/stats/summary` — Returns real-time fest analytics:
  - Total registrations
  - Total participant headcount
  - Breakdown by event (solo vs team counts)
  - Top 10 participating colleges
  - Year-wise participation distribution
- `GET /api/registrations/export/csv` — **Instant CSV spreadsheet download** containing all participant details, contact numbers, emails, and team rosters formatted for Excel & Google Sheets.

### 4. Event-Day Attendance Check-in
- `PATCH /api/registrations/:id/checkin` — Mark a participant or team as checked-in at the venue entrance.

### 5. Inquiries & Contact
- `POST /api/contact` — Submit general inquiries or festival questions.

### 6. System Health
- `GET /api/health` — Check server status and database connectivity.

---

## 🎯 Key Features

- 🌌 **Cosmic Deep Space UI:** Immersive void-black and amber gold theme matching the Srijan visual identity.
- 📱 **Fully Responsive:** Seamlessly adapts to smartphones, tablets, laptops, and wide screens.
- 👥 **Smart Form Validation:** Handles solo entries and dynamic multi-member team rosters with real-time error prevention.
- 🆔 **Auto-Generated Badges:** Provides participants with unique, printable registration confirmation receipts with copyable IDs.
- 🔍 **High-Performance Search:** Database-level compound and full-text indexes for instant lookups during event days.
- 📊 **Organizer Dashboard Ready:** Built-in aggregation endpoints and one-click CSV exports for event coordinators.

---

## 📜 License & Credits

- **Project:** Srijan 2026 Technical Festival Platform
- **Tagline:** *Together, We Create*
- **License:** Proprietary & Developed for the Srijan Technical Festival Organizing Committee.
