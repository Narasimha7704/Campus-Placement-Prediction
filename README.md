# 🎓 Placement Management System

A comprehensive web application designed to streamline the campus placement process. This system facilitates seamless interaction between students, faculty/TPO (Training & Placement Officers), and placement drives, automating many manual tasks and providing valuable insights.

## 🚀 Overview

The Placement Management System serves as a central hub for all placement-related activities. It empowers:
- **Students** to build professional resumes, track applications, and prepare for interviews with AI-powered tools.
- **Faculty** to manage student data, organize placement drives, track enrollments, and analyze placement statistics.
- **Admins** to oversee the entire system.

## ✨ Key Features

### 👨‍🎓 For Students
- **Smart Dashboard**: Real-time overview of profile completion, available drives, and application status.
- **AI-Powered Resume Builder**:
  - **Quick Fill**: Auto-fill profile by uploading an existing resume (PDF/TXT).
  - **ATS Score Checker**: Analyze resume compatibility with Applicant Tracking Systems using AI (Llama 3.1).
  - **Company-Specific Resumes**: Generate tailored resumes for specific companies.
  - **Templates**: Choose from multiple professional templates (ATS Classic, Modern Professional).
- **Drive Management**: View and apply for upcoming placement drives.
- **Analytics**: Track personal application progress.

### 👨‍🏫 For Faculty / TPO
- **Comprehensive Dashboard**: High-level view of placement stats (Total Students, Placed %, Avg CTC, Active Drives).
- **Student Management**: View, filter, and manage student profiles and placement status.
- **Drive Management**: Create and manage placement drives with specific criteria.
- **Enrollment Tracking**: Monitor student enrollments for each drive.
- **Excel Usage**: Bulk upload student data via Excel/CSV.
- **Analytics & Reports**: Detailed insights into placement performance.

### 🤖 Tech Stack

#### Frontend
- **React.js**: Core framework for building the user interface.
- **Vite**: Fast build tool and development server.
- **Firebase**: Authentication (Email/Password) and Firestore Database.
- **Lucide React**: Modern iconography.
- **Chart.js / Recharts**: Data visualization for analytics.
- **HTML2PDF / PDF.js**: Resume generation and parsing.

#### Backend
- **Node.js & Express**: API server for handling business logic.
- **Firebase Admin SDK**: Secure server-side validation and database operations.
- **OpenRouter API**: AI integration for ATS scoring and resume analysis (Llama 3.1).
- **Multer**: File handling for uploads.

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v18+)
- Firebase Project (with Firestore and Auth enabled)
- OpenRouter API Key (for AI features)

### 1. Repository Setup
\`\`\`bash
git clone <repository-url>
cd Placements-drive-application
\`\`\`

### 2. Backend Setup
\`\`\`bash
cd placement-backend
npm install

# Create .env file
echo "OPENROUTER_API_KEY=your_key_here" > .env
echo "PORT=5001" >> .env
echo "NODE_ENV=development" >> .env

# Run Server
npm run server
\`\`\`
*Backend runs on port **5001***

### 3. Frontend Setup
\`\`\`bash
cd placement-frontend
npm install

# Create .env file (if not exists)
# Add your Firebase config and API URL
# VITE_API_URL=http://localhost:5001

# Run Frontend
npm run dev
\`\`\`
*Frontend runs on port **3000***

## 📝 Usage Guide

### Authentication
- **Students**: Sign up/Login using email.
- **Faculty/Admin**: Accounts are typically pre-created or require specific role assignment in Firebase.

### ATS Score Checker
1. Go to Student Dashboard > Quick Actions > ATS Score Checker.
2. Upload your resume (PDF/TXT).
3. The system analyzes it using AI and provides a score (0-100), grade, and actionable feedback.

### Resume Builder
1. Go to "Generate Resume" or "Company Resume".
2. Fill in details (or use Quick Fill).
3. Select a template and download as PDF.

## 📄 License
This project is licensed under the [MIT License](LICENSE).

---
*Built with ❤️ for Campus Placements*
