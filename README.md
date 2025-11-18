🚀 PeerNova — Centralized Campus Collaboration Platform

PeerNova is a comprehensive digital platform designed to centralize student communication, collaboration, and resource sharing within a campus ecosystem. It solves the scattered nature of college communication by providing one unified space where students can connect, discover peers, share academic materials, engage with events, and explore opportunities—all supported by intelligent search, filtering, and personalized recommendations.

📌 Table of Contents

Overview

Problem Statement

Features

System Architecture

Tech Stack

API Overview

Installation & Setup

Environment Variables

Folder Structure

Contributing

License

1️⃣ Overview

PeerNova aims to bring together all aspects of college interaction—academics, community, collaboration, and events—into a single, seamless platform. The platform enables students to:

Discover peers across departments

Share and access academic resources

Join or create study groups

Explore campus events

Communicate efficiently using a centralized feed

Leverage intelligent search and filtering features

2️⃣ Problem Statement

Students often face issues like:

❌ Fragmented Communication

Information spread across WhatsApp, email, and multiple platforms.

❌ Limited Peer Discovery

Hard to connect with students outside one’s class or circle.

❌ Inefficient Resource Sharing

No centralized place to share notes, materials, or study files.

❌ Event Discovery Gap

College events are often missed due to poor visibility.

❌ Collaboration Overhead

Forming study groups or project teams is unorganized and time-consuming.

✔ PeerNova solves all of these through:

A centralized communication hub

Intelligent search & filtering

Community-driven collaboration spaces

Unified resource library

Engaging event discovery experience

3️⃣ System Architecture
🔄 Architecture Flow
User (React Frontend)
        ↓
API Gateway (Express.js Backend)
        ↓
Business Logic Layer + Search Engine
        ↓
MongoDB Database
        ↓
External Services (Nodemailer, Cloudinary)

🔧 Technologies in Each Layer

Frontend: React.js, React Router, Axios

Backend: Node.js + Express.js

Database: MongoDB (NoSQL)

Authentication: JWT-based

File Uploads: Cloudinary

Emails: Nodemailer

Hosting:

Frontend → Vercel / Netlify

Backend → Render / Railway

Database → MongoDB Atlas

🧭 Example System Flow
User enters search → API (/api/search)
→ MongoDB Query (filters + pagination)
→ Sorted results returned
→ Render on FE with infinite scroll
→ (Optional) Email notifications triggered

4️⃣ Key Features
🔐 Authentication & Profiles

Secure signup/login (JWT-based)

Email verification

Student & Admin roles

Editable profiles: bio, photo, department, major, interests

🔍 Discovery & Search

Global keyword search (users, posts, groups, events)

Advanced filters (department, tags, date range)

Sorting (relevance, latest, popularity)

Student directory

📰 Community Feed

Create posts: text + images + tags

Like, comment, share

Personalized feed based on interests

Tagging system for discoverability

👥 Study Groups

Create subject-based or interest-based groups

Join/leave groups

Group management for admins

Group-specific discussion feed

📚 Resource Sharing

Upload notes, PDFs, documents (Cloudinary)

Searchable resource library

Document metadata

Filters: subject, type, upload date

🎉 Event Hub

Create and manage events

Browse by date, category, tags

RSVP system

Email reminders

⚡ Performance

Infinite scroll

Pagination

Lazy-loaded images

🔔 Notifications

Real-time alerts

Email digests

Notification preferences

5️⃣ Tech Stack
🖥 Frontend

React.js

React Router

TailwindCSS

React Query

Axios

🛠 Backend

Node.js

Express.js

Middlewares: CORS, Helmet, Rate Limiter, Compression

🗄 Database

MongoDB

Mongoose ORM

🔑 Authentication

JWT

bcryptjs

🔎 Search & Filtering

MongoDB Text Indexes

Aggregation Pipeline

☁ File & Emails

Cloudinary

Nodemailer

📜 Documentation

Swagger / OpenAPI

6️⃣ API Overview (Authentication)
Endpoint	Method	Description	Access
/api/auth/signup	POST	Register new user with email verification	Public
/api/auth/login	POST	Authenticate user, return JWT	Public
/api/auth/logout	POST	Logout user, invalidate token	Auth
/api/auth/refresh	POST	Refresh expired token	Auth

(Can generate full API docs if you want.)

7️⃣ Installation & Setup
🔧 Clone the repository
git clone https://github.com/your-username/peernova.git
cd peernova

📦 Install dependencies
Backend:
cd backend
npm install

Frontend:
cd frontend
npm install

▶ Run Backend
npm run dev

▶ Run Frontend
npm start

8️⃣ Environment Variables

Create a .env file in backend:

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

9️⃣ Folder Structure (Backend)
/backend
|-- src
|   |-- config/
|   |-- controllers/
|   |-- routes/
|   |-- models/
|   |-- middleware/
|   |-- utils/
|   |-- index.js
|-- package.json

🤝 Contributing

Contributions are welcome!
Please create a pull request and describe your changes clearly.

📄 License

This project is licensed under the MIT License.