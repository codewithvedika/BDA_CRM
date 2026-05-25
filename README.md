BDA CRM - Sales Pipeline Management System

---

FEATURES

- Login and Register with JWT authentication
- Role based access control (Admin and BDA Employee)
- Dashboard with KPI cards and charts
- Lead management with search and filters
- Kanban pipeline board with drag and drop
- Task and follow-up management
- Notes and comments on leads
- Activity timeline for each lead
- Team management (Admin only)
- Analytics page with charts
- Send follow-up emails to clients
- File attachments via Cloudinary
- Real-time notifications via Socket.io
- Dark mode support
- Fully responsive design

---

ROLES

Admin
  - View and manage all leads
  - Assign leads to BDA employees
  - Add, edit, delete team members
  - View full analytics and team performance
  - Create tasks for any user

BDA Employee
  - View only their assigned leads
  - Update lead status and add notes
  - Create and complete their own tasks
  - View their personal dashboard

---

PIPELINE STAGES

New Lead > Contacted > Qualified > Proposal Sent > Negotiation > Won / Lost

---

PROJECT STRUCTURE

bda-crm/
  backend/
    config/         - Database connection
    controllers/    - Business logic
    middleware/     - JWT auth middleware
    models/         - Mongoose schemas
    routes/         - API routes
    utils/          - Seeder script
    server.js       - Entry point
    .env.example    - Environment variables template

  frontend/
    src/
      components/   - Reusable components
      context/      - Auth and theme context
      pages/        - All page components
      utils/        - Axios API client
    public/
    tailwind.config.js

---

SETUP AND INSTALLATION

Requirements
  - Node.js version 16 or above
  - MongoDB installed and running locally
  - Git

Step 1 - Clone the repository
  git clone https://github.com/yourusername/bda-crm.git
  cd bda-crm

Step 2 - Install dependencies

  Backend
    cd backend
    npm install

  Frontend
    cd frontend
    npm install

Step 3 - Configure environment variables

Step 4 - Seed the database
  cd backend
  node utils/seeder.js

Step 5 - Run the application

  Start backend (from /backend folder)
    npm run dev

  Start frontend (from /frontend folder)
    npm start

  App runs at http://localhost:3000
  API runs at http://localhost:5000

---

DEMO ACCOUNTS

  Admin
    Email    : admin@bdacrm.com
    Password : admin123

  BDA Employee 1
    Email    : rahul@bdacrm.com
    Password : bda123

  BDA Employee 2
    Email    : sneha@bdacrm.com
    Password : bda123

---

API ENDPOINTS

Auth
  POST   /api/auth/register
  POST   /api/auth/login
  GET    /api/auth/me
  PUT    /api/auth/profile

Leads
  GET    /api/leads
  GET    /api/leads/kanban
  GET    /api/leads/:id
  POST   /api/leads
  PUT    /api/leads/:id
  DELETE /api/leads/:id

Tasks
  GET    /api/tasks
  POST   /api/tasks
  PUT    /api/tasks/:id
  DELETE /api/tasks/:id

Notes
  GET    /api/notes/lead/:leadId
  POST   /api/notes/lead/:leadId
  DELETE /api/notes/:id

Analytics
  GET    /api/analytics/dashboard
  GET    /api/analytics/monthly
  GET    /api/analytics/team-performance
  GET    /api/analytics/pipeline
  GET    /api/analytics/lead-sources

Users (Admin only)
  GET    /api/users
  POST   /api/users
  PUT    /api/users/:id
  DELETE /api/users/:id

---