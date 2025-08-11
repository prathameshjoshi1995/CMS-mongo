<div align="center">

# 🚨 Complaint Management System

### A modern, full-stack complaint tracking and resolution platform

[![Last Commit](https://img.shields.io/github/last-commit/yourusername/cms?style=for-the-badge&color=blue)](https://github.com/yourusername/cms/commits/main)
[![Languages](https://img.shields.io/github/languages/top/yourusername/cms?style=for-the-badge&color=green)](https://github.com/yourusername/cms)
[![License](https://img.shields.io/badge/License-ISC-blue.svg?style=for-the-badge)](https://opensource.org/licenses/ISC)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg?style=for-the-badge&logo=node.js)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-19.1.0-blue.svg?style=for-the-badge&logo=react)](https://reactjs.org/)

</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Built With](#built-with)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

The Complaint Management System (CMS) is a comprehensive full-stack web application designed to streamline the process of filing, tracking, and resolving complaints within organizations. Built with modern technologies, it provides separate interfaces for administrators and regular users, ensuring efficient complaint handling with real-time updates and detailed analytics.

### Key Capabilities:
- **User Authentication & Authorization** - Secure login with role-based access control
- **Complaint Filing** - Intuitive forms for submitting detailed complaints
- **Status Tracking** - Real-time updates on complaint resolution progress
- **Admin Dashboard** - Comprehensive analytics and management tools
- **Department Management** - Organized complaint routing by department
- **Priority System** - Multi-level priority classification (Low, Medium, High, Critical)
- **Comment System** - Internal communication for complaint resolution
- **File Attachments** - Support for document uploads and evidence
- **Analytics & Reporting** - Detailed insights and performance metrics

---

## ✨ Features

### 🔐 Authentication & Security
- JWT-based authentication system
- Role-based access control (Admin/User)
- Password hashing with bcrypt
- Protected routes and middleware
- Session management

### 📝 Complaint Management
- **User Interface:**
  - File new complaints with detailed forms
  - Track complaint status in real-time
  - View complaint history and updates
  - Receive notifications on status changes

- **Admin Interface:**
  - Comprehensive dashboard with analytics
  - Bulk complaint management
  - Department-wise complaint routing
  - Priority-based sorting and filtering
  - Resolution tracking and reporting

### 📊 Analytics & Reporting
- Real-time dashboard with key metrics
- Department-wise complaint distribution
- Priority level analysis
- Resolution time tracking
- Performance analytics

### 🎨 User Experience
- Modern, responsive Material-UI design
- Intuitive navigation and layouts
- Real-time form validation
- Toast notifications for user feedback
- Loading states and error handling

---

## 🛠 Built With

<div align="center">

### Frontend Technologies
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Material-UI](https://img.shields.io/badge/Material--UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)

### Backend Technologies
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=for-the-badge&logo=mongoose&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)
![bcrypt](https://img.shields.io/badge/bcrypt-00A3CC?style=for-the-badge&logo=bcrypt&logoColor=white)

### Development Tools
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white)
![PostCSS](https://img.shields.io/badge/PostCSS-DD3A0A?style=for-the-badge&logo=postcss&logoColor=white)
![Autoprefixer](https://img.shields.io/badge/Autoprefixer-DD3735?style=for-the-badge&logo=autoprefixer&logoColor=white)

</div>

---

## 🚀 Installation & Setup

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local installation or MongoDB Atlas account)

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/cms.git
cd cms
```

### Step 2: Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
```

Configure your `.env` file with the following variables:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/cms
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
```

### Step 3: Frontend Setup

```bash
# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
```

Configure your frontend `.env` file:

```env
VITE_API_URL=http://localhost:5000/api
VITE_APP_NAME=Complaint Management System
```

### Step 4: Database Setup

```bash
# Start MongoDB (if running locally)
mongod

# Run database setup scripts (from backend directory)
cd backend
npm run create-admin
```

### Step 5: Start the Application

#### Option 1: Start Both Servers Manually

```bash
# Terminal 1 - Start Backend
cd backend
npm run dev

# Terminal 2 - Start Frontend
cd frontend
npm run dev
```

#### Option 2: Use the Provided Scripts

```bash
# Windows (PowerShell)
./start-servers.ps1

# Windows (Command Prompt)
start-servers.bat
```

### Step 6: Access the Application

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5000
- **Default Admin Credentials**: 
  - Email: admin@cms.com
  - Password: admin123

---

## 💻 Usage

### For Users

1. **Register/Login**: Create an account or login with existing credentials
2. **File a Complaint**: 
   - Navigate to "File Complaint" page
   - Fill in the complaint form with details
   - Select department and priority level
   - Submit the complaint
3. **Track Status**: Monitor complaint progress in your dashboard
4. **View History**: Access all your submitted complaints

### For Administrators

1. **Login**: Access admin panel with admin credentials
2. **Dashboard**: View comprehensive analytics and metrics
3. **Manage Complaints**:
   - View all complaints with filtering options
   - Update complaint status and assign to departments
   - Add internal comments and resolutions
4. **User Management**: Manage user accounts and permissions
5. **Reports**: Generate detailed reports and analytics

### API Usage Examples

#### Authentication
```javascript
// Login
const response = await fetch('/api/auth/login', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ email, password })
});
```

#### File Complaint
```javascript
// Create new complaint
const complaint = await fetch('/api/complaints', {
  method: 'POST',
  headers: { 
    'Content-Type': 'application/json',
    'Authorization': `Bearer ${token}`
  },
  body: JSON.stringify({
    title: 'Network Issue',
    description: 'Unable to access company network',
    department: 'IT',
    priority: 'High'
  })
});
```

#### Get Complaints
```javascript
// Fetch user complaints
const complaints = await fetch('/api/complaints/user', {
  headers: { 'Authorization': `Bearer ${token}` }
});
```

---

## 📁 Folder Structure

```
CMS/
├── 📁 backend/                    # Backend Node.js/Express server
│   ├── 📁 config/                # Configuration files
│   │   └── db.js                 # Database configuration
│   ├── 📁 controllers/           # Business logic controllers
│   │   ├── authController.js     # Authentication logic
│   │   ├── complaintController.js # Complaint management
│   │   ├── logController.js      # Logging functionality
│   │   └── userController.js     # User management
│   ├── 📁 middleware/            # Custom middleware
│   │   ├── auth.js               # Authentication middleware
│   │   ├── errorHandler.js       # Error handling
│   │   └── logger.js             # Request logging
│   ├── 📁 models/                # MongoDB schemas
│   │   ├── Complaint.js          # Complaint data model
│   │   ├── Log.js                # Log data model
│   │   └── User.js               # User data model
│   ├── 📁 routes/                # API route definitions
│   │   ├── authRoutes.js         # Authentication routes
│   │   ├── complaintRoutes.js    # Complaint routes
│   │   ├── logRoutes.js          # Log routes
│   │   └── userRoutes.js         # User routes
│   ├── 📁 scripts/               # Utility scripts
│   │   ├── createAdmin.js        # Admin user creation
│   │   ├── createTestData.js     # Test data generation
│   │   └── cleanupAndSeed.js     # Database cleanup
│   ├── 📁 services/              # Business services
│   │   └── dbService.js          # Database operations
│   ├── 📁 utils/                 # Utility functions
│   │   ├── jwt.js                # JWT utilities
│   │   └── validators.js         # Input validation
│   ├── index.js                  # Main server file
│   ├── package.json              # Backend dependencies
│   └── start-server.js           # Server startup script
│
├── 📁 frontend/                  # React frontend application
│   ├── 📁 public/                # Static assets
│   ├── 📁 src/                   # Source code
│   │   ├── 📁 components/        # Reusable UI components
│   │   │   ├── 📁 common/        # Common components
│   │   │   ├── 📁 complaints/    # Complaint-specific components
│   │   │   ├── 📁 dashboard/     # Dashboard components
│   │   │   ├── 📁 Header/        # Header components
│   │   │   ├── 📁 Sidebar/       # Sidebar components
│   │   │   └── 📁 users/         # User management components
│   │   ├── 📁 context/           # React context providers
│   │   │   └── AuthContext.jsx   # Authentication context
│   │   ├── 📁 data/              # Static data files
│   │   ├── 📁 hooks/             # Custom React hooks
│   │   ├── 📁 layout/            # Layout components
│   │   ├── 📁 pages/             # Page components
│   │   │   ├── 📁 admin/         # Admin pages
│   │   │   ├── 📁 auth/          # Authentication pages
│   │   │   └── 📁 user/          # User pages
│   │   ├── 📁 routes/            # Routing configuration
│   │   ├── 📁 utils/             # Utility functions
│   │   ├── App.jsx               # Main App component
│   │   └── main.jsx              # Application entry point
│   ├── package.json              # Frontend dependencies
│   └── vite.config.js            # Vite configuration
│
├── 📁 documents/                 # Project documentation
│   ├── dependencies-and-hooks.txt # Dependencies overview
│   ├── project-overview.txt      # Detailed project overview
│   └── user-manual.txt           # User manual
│
├── start-servers.bat             # Windows batch script
├── start-servers.ps1             # PowerShell script
└── README.md                     # This file
```

---

## 🔌 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/register` | User registration |
| `POST` | `/api/auth/login` | User login |
| `POST` | `/api/auth/logout` | User logout |
| `GET` | `/api/auth/me` | Get current user |

### Complaints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/complaints` | Get all complaints (Admin) |
| `GET` | `/api/complaints/user` | Get user's complaints |
| `POST` | `/api/complaints` | Create new complaint |
| `GET` | `/api/complaints/:id` | Get specific complaint |
| `PUT` | `/api/complaints/:id` | Update complaint |
| `DELETE` | `/api/complaints/:id` | Delete complaint |

### Users (Admin Only)
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/users` | Get all users |
| `GET` | `/api/users/:id` | Get specific user |
| `PUT` | `/api/users/:id` | Update user |
| `DELETE` | `/api/users/:id` | Delete user |

### Logs (Admin Only)
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/logs` | Get system logs |
| `GET` | `/api/logs/:id` | Get specific log |

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow the existing code style and conventions
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

---

## 📄 License

This project is licensed under the **ISC License** - see the [LICENSE](LICENSE) file for details.

<div align="center">

---

**Made with ❤️ by [Your Name]**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourusername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yourusername)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/yourusername)

</div>
#   C M S - m o n g o  
 