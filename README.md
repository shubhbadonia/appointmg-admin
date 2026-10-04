# AppointMG Admin

AppointMG Admin is the admin dashboard for an appointment management application built with React, Vite, and Tailwind CSS. It allows administrators to manage doctors, view appointment data, and monitor the overall clinic workflow. The dashboard also supports a doctor role with a dedicated interface for appointment management and profile updates.

## Overview

This frontend connects to the AppointMG backend API to handle:

- Admin login and session management
- Doctor registration and availability control
- Appointment listing and cancellation
- Dashboard metrics for doctors, appointments, and patients
- Doctor-specific appointment management and profile views

## Features

### Admin features

- Secure admin login
- Dashboard summary cards for total doctors, appointments, and patients
- View all appointments across the clinic
- Cancel appointments
- Add new doctors with profile image, experience, fees, speciality, address, and bio
- View all doctors and toggle their availability status

### Doctor features

- Doctor login
- Doctor dashboard with appointment and summary data
- View doctor appointments
- Mark appointments as complete or cancel them
- Update and view doctor profile information

## Tech Stack

- React 18
- Vite 5
- Tailwind CSS
- React Router DOM
- Axios for API calls
- React Toastify for notifications

## Project Structure

```bash
appointmg-admin/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── context/
│   ├── pages/
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env
├── .eslintrc.cjs
├── .gitignore
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── vercel.json
├── vite.config.js
└── README.md
```

## Environment Variables

Create a `.env` file in the project root with the backend URL:

```env
VITE_CURRENCY=$
VITE_BACKEND_URL=https://appointmg-backend.onrender.com
```

You can also switch to a local backend during development:

```env
VITE_BACKEND_URL=http://localhost:4000
```

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Start the development server

```bash
npm run dev
```

### 3. Build for production

```bash
npm run build
```

### 4. Preview production build

```bash
npm run preview
```

## Demo Credentials

The app includes demo accounts as shown in the login UI:

- Admin
  - Email: admin@appointmg.com
  - Password: admin12345

- Doctor
  - Email: aarav@appointmg.com
  - Password: aarav12345

## Roles and Flow

### Admin

The admin user can:

- log in
- see the clinic overview dashboard
- review bookings by date and patient
- manage doctor profiles and availability
- register a new doctor

### Doctor

The doctor user can:

- log in separately
- review their appointment list
- mark visits as complete
- cancel bookings when needed
- access their profile section

## Backend Integration

This project expects the AppointMG backend API to expose endpoints such as:

- `/api/admin/login`
- `/api/doctor/login`
- `/api/admin/dashboard`
- `/api/admin/appointments`
- `/api/admin/all-doctors`
- `/api/admin/add-doctor`
- `/api/admin/change-availability`
- `/api/doctor/appointments`
- `/api/doctor/profile`
- `/api/doctor/cancel-appointment`
- `/api/doctor/complete-appointment`

## Notes

- The project is designed as a dashboard for a clinic appointment system.
- It is strongly tied to a backend service and uses token-based authentication stored in local storage.
- Styling is done primarily with Tailwind CSS and custom utility classes.

## License

This project is currently unlicensed unless added by the repository owner.

## Repository Context

This repository contains the frontend/admin portal of the AppointMG platform. For the complete system, you would typically pair it with the AppointMG backend service that handles business logic, authentication, doctor data, and appointment persistence.
