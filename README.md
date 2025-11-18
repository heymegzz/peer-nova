🚀 PeerNova — Centralized Campus Collaboration Platform

PeerNova is a comprehensive digital platform designed to centralize student communication, collaboration, and resource sharing within campus ecosystems. It solves the fragmented nature of student interactions by providing one unified space where students can discover peers, share academic resources, join study groups, and explore campus events with intelligent search, filtering, and sorting capabilities.

📌 Table of Contents

Overview

Problem Statement

System Architecture

Key Features

Tech Stack

API Overview

Installation & Setup

Environment Variables

Folder Structure

Contributing

License

🧭 Overview

PeerNova brings together all aspects of campus interaction—community feed, peer discovery, resource sharing, events, and study groups—into a seamless digital platform.

❗ Problem Statement

Students face several challenges in current college ecosystems:

Fragmented Communication: Information spread across WhatsApp groups, emails, and multiple platforms.

Limited Peer Discovery: Hard to discover students outside immediate classes.

Inefficient Resource Sharing: No centralized area for notes, PDFs, study files.

Event Discovery Gap: Students miss campus events due to scattered announcements.

Unorganized Collaboration: Struggles in forming study groups or coordinating projects.

PeerNova solves these through a centralized, intelligent, and collaborative platform.

🏗 System Architecture
Architecture Flow
User (React Frontend)
        ↓
API Gateway (Express.js Backend)
        ↓
Business Logic Layer + Search Engine
        ↓
MongoDB (Database)
        ↓
External Services (Nodemailer, Cloudinary)

Technology Description

Frontend: React.js, React Router, Axios

Backend: Node.js + Express.js

Database: MongoDB (NoSQL)

Authentication: JWT-based login/signup

Notifications: Nodemailer for sending reminders

Hosting:

Frontend → Vercel / Netlify

Backend → Render / Railway

Database → MongoDB Atlas

Example Flow
User Search Query
→ React App
→ /api/search (Express endpoint)
→ MongoDB Query with Filters + Pagination
→ Sorted Results sent back
→ Display with Infinite Scroll
→ Optional Email Notifications triggered

⭐ Key Features
🔐 Authentication & Profiles

JWT-based secure login/signup

Email verification

Student/Admin roles

Editable profiles (bio, image, department, interests, academic year)

🔍 Discovery & Search

Global search across users, posts, groups, and events

Advanced filtering (department, category, tags, date range)

Sorting (relevance, latest, popularity, trending)

Student directory

📰 Community Feed

Create posts with text, images, and tags

Like, comment, share

Tag-based discoverability

Personalized feed based on interests

👥 Study Groups

Create subject/project/interest-based groups

Join/leave groups

Group admin controls

Group-specific feeds

📚 Resource Sharing

Upload notes, PDFs, links, files (via Cloudinary)

Resource library with search + metadata

Popularity tracking

Filters: subject, file type, upload date

🎉 Event Hub

Create hackathons, fests, workshops, seminars

Event discovery by date, category, interests

RSVP system + reminders

Event filters + sorting options

⚡ Performance Optimization

Infinite scroll

Pagination

Lazy loading of media

🔔 Notifications

Real-time alerts

Email digests for important updates

Customizable notification preferences

🧰 Tech Stack
Frontend

React.js

React Router

TailwindCSS

Axios

React Query

Backend

Node.js

Express.js

CORS, Compression, Rate Limiting

Database

MongoDB

Mongoose

Authentication

JWT

bcryptjs

Others

Cloudinary (File Uploads)

Nodemailer (Emails)

Joi / Express-validator

dotenv

Swagger (API documentation)

📡 API Overview (Auth)
Endpoint	Method	Description	Access
/api/auth/signup	POST	Register user with email verification	Public
/api/auth/login	POST	Login, returns JWT token	Public
/api/auth/logout	POST	Log out user	Authenticated
/api/auth/refresh	POST	Refresh JWT token	Authenticated
🛠 Installation & Setup
Clone Repository
git clone https://github.com/your-username/peernova.git
cd peernova

Install Dependencies
Backend
cd backend
npm install

Frontend
cd frontend
npm install

Run Backend
npm run dev

Run Frontend
npm start

🔑 Environment Variables

Create a .env file inside backend:

PORT=
MONGO_URI=
JWT_SECRET=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
EMAIL_HOST=
EMAIL_USER=
EMAIL_PASS=
FRONTEND_URL=

📁 Folder Structure
/backend
│── src/
│   ├── config/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── utils/
│   └── index.js
│
└── package.json

🤝 Contributing

Contributions are always welcome!
Please open an issue or submit a pull request.

📄 License

This project is licensed under the MIT License.
