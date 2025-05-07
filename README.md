# 🏏 MeetX Backend - Activity Booking API

This is a simple REST API for a basic **Activity Booking App**, developed as part of the MeetX Backend Developer Internship assignment. It handles user registration/login, public activity listing, and authenticated activity booking.

---

## 🚀 Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB + Mongoose
- **Authentication:** JWT (JSON Web Token)
- **Security:** bcrypt for password hashing
- **Validation:** express-validator

---

## 📁 Folder Structure
meetx-backend/
│
├── controllers/ # Logic for API actions
├── middleware/ # JWT auth middleware
├── models/ # MongoDB models (User, Activity, Booking)
├── routes/ # Route definitions
├── .env # Environment variables
├── server.js # Entry point
├── package.json
└── README.md

---

## 📦 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/meetx-backend.git
cd meetx-backend

## 2. Install dependencies
npm install

##3. Run the server
npm run dev  # for development (nodemon)
npm start    # for production

##📋 API Endpoints
Auth Routes (/api/auth)
Method	Endpoint	Description	Protected
POST	/register	Register a new user	❌
POST	/login	Login user (get token)	❌

##Activity Routes (/api/activities)
Method	Endpoint	Description	Protected
GET	/	List all activities	❌

##Booking Routes (/api/bookings)
Method	Endpoint	Description	Protected
POST	/:activityId	Book an activity	✅
GET	/me	Get logged-in user's bookings	✅
