# SIEM Security Dashboard

A cybersecurity monitoring and Security Information and Event Management (SIEM) dashboard designed to collect, process, analyze, and visualize security logs. The system detects suspicious activities using predefined security rules and generates severity-based alerts through an interactive dashboard.

## Features

- Security log ingestion and processing
- Log parsing and normalization
- SQLite database storage
- Brute-force attack detection
- Suspicious file-access detection
- Severity-based security alerts
- Source IP tracking
- Log search functionality
- Event type filtering
- Login status filtering
- Interactive security dashboard
- REST API using FastAPI
- Swagger/OpenAPI documentation

## Technologies Used

- Python
- FastAPI
- SQLAlchemy
- SQLite
- React
- Vite
- Axios
- HTML
- CSS
- JavaScript
- Swagger UI / OpenAPI

## System Workflow

Security Logs → Log Ingestion → Parsing → Normalization → Database Storage → Detection Engine → Security Alerts → React Dashboard → Security Monitoring

## Security Detection

### Brute Force Detection

The system detects a potential brute-force attack when 5 or more failed login attempts are detected from the same source IP address.

Example:

Source IP: 192.168.1.15  
Failed Login Attempts: 5  
Severity: HIGH  
Alert: Brute Force Attack

### Suspicious File Access

Successful file-access events are identified and generated as MEDIUM severity alerts for security monitoring.

## Sample Results

- Total Logs: 10
- Failed Logins: 6
- Active Alerts: 2
- Source IPs: 5
- High Severity Alerts: 1

## API Endpoints

- POST `/logs/ingest` — Ingest and process security logs
- GET `/logs/` — Retrieve stored security logs
- GET `/logs/alerts` — Retrieve generated security alerts
- GET `/` — Check API status
- GET `/health` — Check backend health

## Project Structure

SIEM-Security-Dashboard/

├── backend/
│   ├── app/
│   │   ├── routes/
│   │   │   └── logs.py
│   │   ├── services/
│   │   │   ├── parser.py
│   │   │   ├── normalizer.py
│   │   │   ├── detection.py
│   │   │   └── ingestion.py
│   │   ├── main.py
│   │   ├── database.py
│   │   └── models.py
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── logs/
│   └── sample_logs.txt
│
├── README.md
└── .gitignore

## Installation and Setup

### Backend

Clone the repository:

git clone https://github.com/jatinsinghmehta/SIEM-Security-Dashboard.git

cd SIEM-Security-Dashboard

Go to the backend directory:

cd backend

Create a virtual environment:

python -m venv .venv

Activate the virtual environment on Windows PowerShell:

.\.venv\Scripts\Activate.ps1

Install dependencies:

pip install -r requirements.txt

Start the backend:

uvicorn app.main:app --reload

Backend URL:

http://127.0.0.1:8000

Swagger API Documentation:

http://127.0.0.1:8000/docs

### Frontend

Open a new terminal and go to the frontend directory:

cd frontend

Install dependencies:

npm install

Start the frontend:

npm run dev

Dashboard:

http://localhost:5173

## Dashboard

The dashboard provides:

- Total security logs
- Failed login count
- Active security alerts
- Unique source IP count
- High severity alerts
- Log search
- Event filtering
- Login status filtering
- Security logs table
- Security alerts section

## Learning Outcomes

This project provided practical understanding of:

- SIEM fundamentals
- Security log collection
- Log parsing and normalization
- Rule-based threat detection
- Brute-force attack detection
- Security alert generation
- Source IP analysis
- REST API development
- Database integration
- React and FastAPI integration
- Security monitoring concepts

## Future Scope

- Real-time log ingestion
- Additional security detection rules
- Threat intelligence integration
- User authentication
- Role-Based Access Control (RBAC)
- Advanced analytics and charts
- Email and webhook notifications
- Anomaly detection

## Author

Jatin Mehta

Project: SIEM Security Dashboard

Domain: Cybersecurity / Security Information and Event Management

## License

This project was developed for educational and cybersecurity learning purposes.
