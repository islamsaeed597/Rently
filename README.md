<div align="center">
  <img height="150" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExc29lOG5sNDY3eHNneWZ2aGRsOGZydTNwMzkwMzh5MndveHRtZjF2cCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/L1R1tvI9svkIWwpVYr/giphy.gif" alt="Rently Banner" />
</div>

###

<div align="center">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License" />
</div>

###

<h1 align="center">🚀 Rently - Smart Rental Platform</h1>

###

<h3 align="left">📋 About The Project</h3>

<p align="left">
<b>Rently</b> is a modern, full-stack rental marketplace platform designed to connect renters and owners seamlessly. <br><br>
What makes Rently stand out is its deep integration with Artificial Intelligence and modern real-time technologies:<br>
- 🆔 <b>Smart KYC (Know Your Customer):</b> Automated Egyptian National ID verification using Optical Character Recognition (OCR) and Computer Vision to ensure users' authenticity.<br>
- 🤖 <b>Rently Expert AI:</b> A built-in AI chatbot powered by Google Gemini API that assists users, answers common questions, and recommends rental products intelligently.<br>
- 💬 <b>Real-time Chat:</b> Live messaging between renters and owners using WebSockets.<br>
- 📅 <b>Smart Booking & Blackouts:</b> Advanced booking system with availability management and scheduling.
</p>

###

<h3 align="left">💻 Tech Stack & Architecture</h3>

<h4 align="left">🎨 Frontend</h4>
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg" height="40" alt="react" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original-wordmark.svg" height="40" alt="tailwind" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" height="30" alt="vite" />
  <img width="12" />
  <img src="https://img.shields.io/badge/React_Router-CA4245?style=flat-square&logo=react-router&logoColor=white" height="30" alt="react-router" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white" height="30" alt="axios" />
</div>

###

<h4 align="left">⚙️ Backend</h4>
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original-wordmark.svg" height="40" alt="nodejs" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original-wordmark.svg" height="40" alt="express" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Socket.io-black?style=flat-square&logo=socket.io&logoColor=white" height="30" alt="socketio" />
  <img width="12" />
  <img src="https://img.shields.io/badge/JWT-black?style=flat-square&logo=JSON%20web%20tokens&logoColor=white" height="30" alt="jwt" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Multer-FF6C37?style=flat-square&logo=npm&logoColor=white" height="30" alt="multer" />
</div>

###

<h4 align="left">🗄️ Database & Cloud</h4>
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" height="40" alt="mysql" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Google_Auth-4285F4?style=flat-square&logo=google&logoColor=white" height="30" alt="google-auth" />
</div>

###

<h4 align="left">🤖 AI & Data Processing (Python Microservice)</h4>
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original-wordmark.svg" height="40" alt="python" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pytorch/pytorch-original-wordmark.svg" height="40" alt="pytorch" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opencv/opencv-original-wordmark.svg" height="40" alt="opencv" />
  <img width="12" />
  <img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=google&logoColor=white" height="30" alt="gemini" />
</div>

###

<h3 align="left">🚀 Installation & Setup</h3>

<p align="left">
Follow these steps to run the project locally on your machine.
</p>

#### 1. Database Setup
1. Create a MySQL database (e.g., `rently`).
2. Import the provided `mysql.sql` file into your database to generate the tables and initial data.

#### 2. Backend Setup
Open the `Backend` directory and install the dependencies:
```bash
cd Backend
npm install
```
*Create a `.env` file in the `Backend` directory and add your environment variables (Database credentials, JWT secret, Gemini API key, Google Client Secret etc.).*

#### 3. AI & Python Microservice Setup (For KYC ID Verification)
You must install the required Python libraries for image processing. Run this in your terminal:
```bash
pip install easyocr opencv-python torch torchvision
```

#### 4. Frontend Setup
Open the `FrontEnd` directory and install the dependencies:
```bash
cd ../FrontEnd
npm install
```

#### 5. Run the Project
You can start both the Frontend and Backend concurrently using a single command from the Backend directory!
```bash
cd ../Backend
npm run dev
```
*The app should now be running. The frontend typically runs on `http://localhost:5173` and the backend on the specified port in your `.env`.*

###

<h3 align="left">🌟 Key AI Features Explained</h3>

<ul align="left">
  <li><b>Identity Verification (OCR):</b> The project uses Python scripts (`extract_id.py`) with <code>EasyOCR</code> to extract Arabic & English text from National ID images. It validates the 14-digit number and searches for specific keywords to verify the authenticity of the card before approving user verification via the Node.js server.</li>
  <li><b>Rently Expert AI:</b> Integrated via the <code>@google/generative-ai</code> package. It acts as an interactive chatbot for the platform, utilizing context grounding to provide accurate rental recommendations and answer user queries with interactive links.</li>
</ul>

###

<div align="center">
  <p>Made with ❤️ for Rently</p>
</div>
