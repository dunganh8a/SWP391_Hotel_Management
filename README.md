🌿 Ngũ Sơn Resort & Spa Management System

A modern Resort & Spa Management Platform built with React + Vite + TailwindCSS and integrated with Spring Boot RESTful APIs.










📖 Project Overview

Ngũ Sơn Resort & Spa Management System is a full-stack web application developed for managing resort operations including:

Room booking
Spa & wellness services
Yoga & therapy reservations
Customer authentication
Booking management
Responsive user experience

This project was developed as part of the SWP391 Course Project by Group 3 - SE2003.

✨ Main Features
🔐 Authentication Module
User Registration
User Login
Forgot Password with OTP Verification
JWT Authentication
Protected Routes
User Profile Management
🏨 Room Booking System
Browse available rooms
View room details
Search & filter rooms
Booking consultation form
Booking confirmation flow
💆 Spa & Wellness Services
Spa booking
Therapy reservation
Yoga session scheduling
Personalized wellness packages
📱 Responsive UI/UX
Mobile-first design
Tablet & Desktop optimization
Modern organic-green theme
Smooth animations & glassmorphism effects
🛠️ Tech Stack
Frontend
ReactJS
Vite
TailwindCSS
React Router DOM
Axios
Lucide React
Backend
Spring Boot
Spring Security
JWT Authentication
RESTful API
Database
SQL Server
Tools & Platforms
Git & GitHub
Postman
VS Code
IntelliJ IDEA
Figma
📂 Project Structure
src/
├── assets/            # Images, icons, static resources
├── components/        # Shared reusable components
├── context/           # Global state management
├── hooks/             # Custom React hooks
├── layouts/           # Layout wrappers
├── pages/             # Main application pages
├── routes/            # Route configuration
├── services/          # API services & Axios config
├── utils/             # Helper functions
└── App.jsx            # Root application
🔌 API Integration

The frontend communicates with the backend using Axios instances configured with:

Base URL configuration
JWT Authorization headers
Axios Interceptors
Centralized error handling
Automatic redirect on 401 Unauthorized

Example:

import axios from "axios";

const api = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
});

api.interceptors.request.use((config) => {
  const token = localStorage.getItem("token");

  if (token) {
    config.headers.Authorization = `Bearer ${token}`;
  }

  return config;
});

export default api;
🔐 Authentication Flow
Register
   ↓
Email Verification (Optional)
   ↓
Login
   ↓
Receive JWT Token
   ↓
Store Token
   ↓
Access Protected Routes
🏨 Booking Workflow
Browse Rooms/Services
        ↓
Select Booking Option
        ↓
Fill Booking Form
        ↓
Submit Booking Request
        ↓
Backend Validation
        ↓
Booking Confirmation
🎨 UI Design Philosophy

The project follows a Natural Organic Green Style inspired by:

Luxury resorts
Wellness retreats
Minimalist eco-design
Design Elements
Soft green palette
Glassmorphism navigation
Elegant typography
Smooth spacing system
Responsive grid layouts
Typography
Outfit
Playfair Display
📸 Preview
Home Page

Add homepage screenshot here

Room Booking

Add booking screenshot here

Spa Services

Add spa page screenshot here

⚙️ Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/your-username/your-repository.git
2️⃣ Install Dependencies
npm install
3️⃣ Start Development Server
npm run dev
4️⃣ Build Production Version
npm run build
🧪 Testing & Verification
Automated Checks
ESLint Validation
npm run lint
Production Build Validation
npm run build
Manual Testing
Responsive layout verification
Authentication flow validation
Booking workflow testing
API error handling checks
OTP verification testing
🔒 Security Features
JWT Authentication
Protected Routes
Password Validation
Token-based Authorization
API Error Handling
Secure Axios Interceptors
🚀 Future Improvements
Online Payment Integration
Admin Dashboard
Real-time Booking Status
Email Notifications
Multi-language Support
Dark Mode
AI-based Recommendation System
👨‍💻 Team Information

Course: SWP391
Project: Resort & Spa Hotel Management System
Class: SE2003
Team: Group 3

📄 License

This project is developed for educational purposes only.

⭐ Acknowledgements

Special thanks to:

SWP391 instructors
Open-source community
React & Spring Boot ecosystem
📬 Contact

For questions or collaboration opportunities:

GitHub: your-github
Email: your-email@example.com
🌟 Project Status

🚧 Currently under active development and backend integration.
