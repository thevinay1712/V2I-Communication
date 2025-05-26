# V2I_Communication - Secure Vehicle-to-Infrastructure Monitoring System

This repository contains the Flask-based server application for **V2I_Communication**, a secure vehicle-to-infrastructure (V2I) system. It enables real-time monitoring, secure data submission from ESP32 devices, and role-based data visualization for doctors and police personnel.

---

## 📁 Project Structure

```
v2i_communication/
├── app.py                    # Main Flask application
├── requirements.txt          # Python package dependencies
├── templates/                # HTML templates
│   ├── base.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
├── static/                   # Static files (optional)
│   ├── css/
│   └── js/
├── instance/                 # SQLite DB (excluded from Git)
├── README.md                 # Project documentation
└── .gitignore                # Git ignored files
```

---

## 🚀 Getting Started

### 1. Clone and Navigate

```bash
git clone https://github.com/your-username/v2i_communication.git
cd v2i_communication
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Environment Variables

```bash
export FLASK_APP=app.py
export FLASK_ENV=development
```

### 5. Initialize the Database

```bash
flask init-db
```

### 6. Create Admin User

```bash
flask create-admin
```

---

## ▶️ Running the Server

```bash
flask run
# or
python app.py
```

Visit: [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

---

## 🔐 Features

- User Authentication (Login & Register)
- Role-Based Access (Doctor/Police)
- Secure API for Vehicle Data from ESP32
- Interactive Map and Data Table
- Future integration of ABE for fine-grained encryption

---

## 📡 ESP32 API Payload

POST to `/api/vehicle_data` with JSON:

```json
{
  "vehicle_id": "ambulance_01",
  "timestamp_device": "2023-10-27T10:30:00Z",
  "latitude": 34.0522,
  "longitude": -118.2437,
  "speed_kmh": 60.5,
  "temperature_c": 37.2,
  "humidity_percent": 45.0,
  "heart_rate_bpm": 88,
  "blood_oxygen_spo2": 98.5,
  "patient_name": "John Doe",
  "medical_id": "MED00123"
}
```

---

## 🔧 Enhancements Roadmap

- Add actual ABE encryption/decryption
- Improve session security
- Add Docker support
- Responsive design improvements

---

## 📄 License

MIT License

---

## 🙌 Acknowledgments

- Flask
- Bootstrap
- Leaflet.js

---

**Project Title:** V2I_Communication

Enabling secure and reliable vehicle-to-infrastructure data transmission.
