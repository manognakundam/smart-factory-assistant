# AutoPlant-OS | Smart Automotive Manufacturing

**A unified digital platform for smarter, safer, and more efficient automobile manufacturing.**

AutoPlant-OS is an Industry 5.0-inspired smart factory management system that connects manufacturing operations, workforce activities, machine data, and AI-assisted support in one platform. It helps factory personnel monitor production, track equipment, manage maintenance, and respond to operational alerts through role-specific dashboards and voice-based assistance.

## 🚀 What It Offers

- **Centralized Factory Dashboard:** View production progress, machine conditions, workforce information, maintenance activities, and operational alerts.
- **Automotive Production Tracking:** Monitor vehicle manufacturing stages, production quantities, workflow progress, and potential bottlenecks.
- **Machine & Sensor Monitoring:** Access machine status and sensor data to improve visibility into equipment conditions.
- **Maintenance Management:** Organize maintenance requests, track their status, and maintain equipment-related information.
- **Workforce Operations:** Support employee management, attendance tracking, task assignments, and department-level organization.
- **Inventory & Supply Visibility:** Monitor material availability, stock conditions, and potential supply requirements.
- **Safety & Alerts:** Surface operational warnings, equipment faults, and safety-related information.
- **AI-Assisted Voice Interaction:** Explore voice commands and spoken responses for production updates, machine status queries, and operational assistance.
- **Energy Monitoring:** Provide a foundation for tracking energy usage and identifying efficiency opportunities.

## 🏭 Designed for Industry 5.0

AutoPlant-OS emphasizes collaboration between people, machines, and intelligent systems. Instead of treating manufacturing modules as isolated functions, it brings key operational information into a shared environment.

The platform is designed around three user roles:

| Role | Primary Focus |
|---|---|
| Worker | Assigned tasks, attendance, and safety information |
| Manager | Production, equipment, maintenance, and operational monitoring |
| Administrator | User records, roles, departments, and system management |

## 🧠 AI & Voice Assistant

The assistant is intended to make factory information easier to access through natural, voice-based interaction.

Example queries include:

- “What is today's production status?”
- “Check the machine status.”
- “Show active alerts.”
- “Which machines require maintenance?”

Speech recognition and speech synthesis support the voice interaction experience, while AI-assisted functionality is intended to help users interpret operational information and navigate factory workflows.

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | Python, FastAPI |
| API Server | Uvicorn |
| Database | PostgreSQL |
| Database Driver | psycopg2 |
| Configuration | python-dotenv |
| AI Integration | Groq API integration/concept |

## 🏗️ How It Works

The application follows a three-layer architecture:

1. **Frontend:** Provides the dashboards, navigation, login interface, charts, tables, and interactive manufacturing modules.
2. **Backend:** Uses FastAPI to handle API requests, authentication logic, database connectivity, and operational data retrieval.
3. **Database:** Uses PostgreSQL to organize information related to users, departments, machines, attendance, tasks, production, sensors, maintenance, and alerts.

The frontend communicates with the backend through API endpoints, while the backend retrieves and manages the relevant database records.

## 📂 Project Structure

```text
AutoPlant-OS/
├── autoplant-os-light-theme.html
├── backend/
│   └── main.py
├── .env
├── .venv/
└── run.bat
```

- `autoplant-os-light-theme.html` — Main application interface and client-side functionality.
- `backend/main.py` — FastAPI application, API endpoints, and database integration.
- `.env` — Environment-specific database configuration.
- `.venv/` — Python virtual environment.
- `run.bat` — Application startup helper.

## ⚙️ Getting Started

### Prerequisites

- Python installed
- PostgreSQL installed and running
- Git
- A code editor such as Visual Studio Code

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/AutoPlant-OS.git
cd AutoPlant-OS
```

### 2. Create and activate a virtual environment

On Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install backend dependencies

```bash
python -m pip install fastapi uvicorn psycopg2-binary python-dotenv
```

### 4. Configure the database

Create a PostgreSQL database for the application and configure your `.env` file:

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=autoplant_os
DB_USER=postgres
DB_PASSWORD=your_password
```

Replace the example credentials with your local PostgreSQL settings.

**Security note:** Never commit `.env`, database passwords, or API keys to a public repository.

### 5. Start the backend

From the project directory:

```bash
cd backend
python -m uvicorn main:app --reload
```

Open the application at:

- Frontend/API root: http://127.0.0.1:8000
- Backend test endpoint: http://127.0.0.1:8000/api/test

The application requires a correctly configured database and the necessary project data to operate as intended.

## 🔌 API Overview

The backend exposes REST endpoints for accessing major manufacturing modules.

| Endpoint | Purpose |
|---|---|
| `POST /api/login` | Employee login |
| `GET /api/users` | Retrieve user information |
| `GET /api/machines` | Retrieve machine records |
| `GET /api/departments` | Retrieve department information |
| `GET /api/production` | Retrieve production information |
| `GET /api/attendance` | Retrieve attendance records |
| `GET /api/tasks` | Retrieve assigned tasks |
| `GET /api/maintenance` | Retrieve maintenance requests |
| `GET /api/sensors` | Retrieve sensor data |
| `GET /api/alerts` | Retrieve system alerts |

## 🔒 Security Considerations

AutoPlant-OS is an academic and development-oriented implementation. Before deployment in a real manufacturing environment, it should be strengthened with secure password hashing, robust authentication, server-side role authorization, HTTPS, input validation, audit logging, and appropriate database access controls.

## 🔮 Future Improvements

Potential extensions include:

- IoT sensor integration for live machine telemetry
- Machine-learning-based anomaly detection
- More advanced predictive maintenance
- Real-time production notifications
- Enhanced voice assistant capabilities
- Historical production and energy analytics
- Mobile-friendly dashboards
- Docker-based deployment and cloud hosting

## 🎯 Project Goal

AutoPlant-OS explores how web technologies, centralized operational data, and AI-assisted interfaces can support the digital transformation of automotive manufacturing.

**The vision:** Bring production, people, machines, and intelligence together to create a more connected, responsive, and human-centric factory.

**Project Status:** Active development

*Note: Some capabilities are foundational modules or planned enhancements; actual availability depends on the current implementation and integrations.*
