🚀 SRMAP Student Portal API – FastAPI Backend

A complete REST API wrapper for the SRMAP Student Portal with 40+ endpoints covering academics, finance, hostel, SAP, transport, course registration, and more.

✨ Highlights

🔐 Login + Captcha authentication

📚 Academic data (CGPA, attendance, timetable, marks)

💰 Fees & finance details

🏠 Hostel & 🚌 Transport management

📝 Course & SAP registration

⚙️ Clean REST architecture

📄 Swagger & ReDoc auto-documentation

🌐 CORS supported, frontend-ready

📦 Requirements

Python 3.8+

pip

⚙️ Setup & Run
```
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000   # or python main.py
```
🔑 Authentication Flow

1️⃣ Get Captcha
```
GET /api/captcha
```
2️⃣ Login
```
POST /api/login
{
  "username": "AP24110012177",
  "password": "your_password",
  "captcha": "ABC12",
  "session_id": "uuid-from-captcha"
}
```
3️⃣ Logout
```
DELETE /api/logout

```
🏗 Structure
```
.
├── main.py              # FastAPI app (40+ APIs)
├── requirements.txt
├── README.md
├── apis.txt             # Portal HTML reference
└── loginapi.txt
```
🔒 Security Notes

Use DB/Redis for session storage in production

Configure CORS origins

Prefer HTTPS

Add rate limiting

Store secrets in .env

⭐ Get Started
```
pip install -r requirements.txt
python main.py
# Open 👉 http://localhost:8000/docs
```
