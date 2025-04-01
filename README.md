# LinkTree Clone - Analytics and Link Management System

## Overview
The **LinkTree Clone** is a **MERN stack-based** link management platform that allows users to create a personalized link page, manage links, and track analytics for link clicks. It includes user authentication, profile customization, analytics tracking, and an interactive dashboard.

## Features
- **User Authentication** (JWT-based login/signup)
- **Profile Management** (Set and update username, category, and appearance settings)
- **Link Management** (Create, update, delete, and organize links)
- **Redirection System** (Links redirect users to the original URLs)
- **Analytics Tracking**:
  - Track total clicks per link
  - Capture **device type**, **timestamp**, and **unique views** using IP & cookies
  - Display analytics in an interactive dashboard with visual charts
- **Secure API Endpoints** (Protected routes with authentication middleware)
- **Responsive UI** (Works seamlessly on desktop and mobile devices)

## Tech Stack
### Frontend
- **React (Vite)** – For a fast and optimized user interface
- **CSS** – Custom styles for responsiveness
- **Recharts** – For interactive analytics charts

### Backend
- **Node.js & Express.js** – API development
- **MongoDB & Mongoose** – Database management
- **JWT Authentication** – Secure user authentication
- **Multer** – File handling for profile pictures (optional)

## Installation & Setup
### Prerequisites
Make sure you have the following installed:
- Node.js (Latest LTS version)
- MongoDB (Local or Atlas)
- npm or yarn

### Backend Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/linktree-clone.git
   cd linktree-clone/backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file and configure the following:
   ```env
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=5000
   CLIENT_URL=http://localhost:5173
   ```
4. Run the backend server:
   ```sh
   npm start
   ```

### Frontend Setup
1. Navigate to the frontend folder:
   ```sh
   cd ../frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file and configure the following:
   ```env
   VITE_API_URL=http://localhost:5000
   ```
4. Run the frontend development server:
   ```sh
   npm run dev
   ```

## API Endpoints
### Authentication
- `POST /api/auth/register` – Register a new user
- `POST /api/auth/login` – Login with username & password

### Profile
- `GET /api/profile` – Get user profile details
- `PUT /api/profile` – Update username, category, and appearance

### Links
- `POST /api/links` – Create a new link
- `GET /api/links` – Retrieve all user links
- `PUT /api/links/:id` – Update a link
- `DELETE /api/links/:id` – Delete a link
- `GET /:username` – Retrieve user’s public link page

### Analytics
- `GET /api/analytics/:linkId` – Get analytics for a specific link
- `GET /api/analytics?user=username` – Get analytics for all user links

## Future Improvements
- Add role-based access control
- Custom domain integration
- Dark mode theme


