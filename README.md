# Neu1one AI Job Seeker 🚀

Neu1one AI is an intelligent, conversational career coach and job search application. Built with a modern glassmorphism UI, it leverages the power of the Google Gemini API to analyze resumes, provide tailored career advice, and systematically search across top recruitment platforms for active job roles.

## ✨ Features

- **Conversational AI Interface:** Chat naturally with an AI expert targeted specifically at job hunting and career progression.
- **Smart Resume Parsing & Memory:** Upload your resume (PDF/DOC) directly into the chat and the AI will analyze it against active roles. The AI will securely memorize your resume context for the entire chat session.
- **Permanent "Smart" Links:** Completely eliminates `404 Not Found` errors by generating direct Company Search links instead of volatile, highly-expirable single Job IDs.
- **Interactive Job Tracker:** Every generated job application link features an inline interactive "⭐ Save" button, allowing you to visually toggle and track which jobs you want to apply to!
- **Dual Authentication System:** Allows users to log in seamlessly via **Google Sign-In** or by creating an account locally using **Email & Password** verification.
- **Cloud Chat History:** Automatically saves, synchronizes, and segments your chat sessions per-user using Firebase Firestore, allowing you to pick up exactly where you left off.
- **Error Shielding:** Built-in safeguards to detect, intercept, and visually disable broken or expired internal redirect URLs produced by live web-scraping.

## 🛠️ Tech Stack

- **Frontend Framework:** React 18, Vite
- **Styling:** Vanilla CSS & Tailwind CSS (Utility classes)
- **Icons:** Lucide React
- **AI Integration:** Google GenAI SDK (`gemini-1.5-flash`) + Google Search Grounding Tool
- **Backend & Auth:** Firebase (Authentication and Firestore)
- **Markdown Rendering:** React-Markdown with Custom Interactive Elements

## ⚙️ Getting Started

### 1. Requirements
Ensure you have Node.js installed on your machine.

### 2. Installation
Clone the project and install all top-level Node dependencies.
```bash
npm install
```

### 3. Environment Setup
Create a `.env` file at the root of the project alongside `package.json` and provide your API keys to enable the AI and Database functionality:

```env
# Google AI Studio
VITE_GOOGLE_GENAI_API_KEY="your_google_genai_api_key"

# Firebase Web configuration
VITE_FIREBASE_API_KEY="your_firebase_api_key"
VITE_FIREBASE_AUTH_DOMAIN="your_firebase_auth_domain"
VITE_FIREBASE_PROJECT_ID="your_firebase_project_id"
VITE_FIREBASE_STORAGE_BUCKET="your_firebase_storage_bucket"
VITE_FIREBASE_MESSAGING_SENDER_ID="your_firebase_messaging_sender_id"
VITE_FIREBASE_APP_ID="your_firebase_app_id"
```

### 4. Setting up Firebase
- Head to your [Firebase Console](https://console.firebase.google.com/).
- Initialize a **Cloud Firestore Database** (Rules must allow reads/writes for logged-in users).
- Initialize **Firebase Authentication** and explicitly enable both **Google Sign-In** and **Email/Password** as active providers.

### 5. Running the Application
Start the development server:
```bash
npm run dev
```
Open up your browser and navigate to `http://localhost:3000/` to use the application!

## 🗑️ Managing History
- To delete an individual search history item, simply hover over the title in the sidebar and click the `X`.
- To completely wipe your chat records from the database, use the `Trash` button next to "Search History".

---
*Developed as a premier AI-powered Job Assistant.*
