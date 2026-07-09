<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=220&section=header&text=VIRTUAL%20COURSES&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Learn.%20Teach.%20Grow.%20—%20A%20Full%20Stack%20Online%20Learning%20Platform&descAlignY=58&descSize=17&descColor=E0E0E0)

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=2500&pause=900&color=6C63FF&center=true&vCenter=true&width=650&lines=MERN+Stack+E-Learning+Platform;Course+Creation+%2B+Sales+%2B+Payments;AI-Powered+Course+Search;Built+by+Biswajit+Pattanaik" alt="Typing SVG" />

<br/><br/>

<p>
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Node.js-Express-339933?logo=node.js&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248?logo=mongodb&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/TailwindCSS-4-06B6D4?logo=tailwindcss&logoColor=white&style=for-the-badge" />
</p>
<p>
  <img src="https://img.shields.io/badge/Vercel-Frontend-black?logo=vercel&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Render-Backend-46E3B7?logo=render&logoColor=black&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Cloudinary-Media-3448C5?logo=cloudinary&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Razorpay-Payments-0C2451?logo=razorpay&logoColor=white&style=for-the-badge" />
</p>

<p>
  <img src="https://img.shields.io/github/stars/Biswajitpa/Virtual-Course?style=for-the-badge&color=6C63FF" />
  <img src="https://img.shields.io/github/last-commit/Biswajitpa/Virtual-Course?style=for-the-badge&color=6C63FF" />
  <img src="https://img.shields.io/badge/status-active-success?style=for-the-badge&color=6C63FF" />
</p>

</div>

<br/>

## 📖 Overview

**Virtual Courses** is a production-grade **MERN stack e-learning platform** where **educators** create and sell structured video courses, and **students** discover, purchase, and learn from them. It combines secure authentication, cloud media handling, real payment processing, and AI-assisted discovery into one cohesive product — architected the way a real SaaS learning platform would be.

<br/>

## 🏗️ System Architecture

```mermaid
flowchart TB
    subgraph Client["🖥️ Client Layer"]
        A[React + Vite SPA<br/>Deployed on Vercel]
        A1[Redux Toolkit — State]
        A2[React Router — SPA Routing]
        A --> A1
        A --> A2
    end

    subgraph Edge["🌐 Network Layer"]
        B[HTTPS + CORS<br/>Cross-Origin Auth Cookies]
    end

    subgraph Server["⚙️ Application Layer — Render"]
        C[Express.js REST API]
        C1[Auth Middleware<br/>JWT Verification]
        C2[Multer<br/>File Upload Handler]
        C3[Route Controllers<br/>auth · user · course · payment · ai · review]
        C --> C1 --> C3
        C --> C2 --> C3
    end

    subgraph Data["🗄️ Data & Storage Layer"]
        D[(MongoDB Atlas<br/>Users · Courses · Reviews)]
        E[Cloudinary<br/>Images & Video Assets]
    end

    subgraph External["🔌 External Services"]
        F[Firebase Auth<br/>Google Sign-In]
        G[Razorpay<br/>Payment Gateway]
        H[Nodemailer<br/>OTP / Email]
        I[Gemini AI API<br/>Smart Course Search]
    end

    A -- "Axios REST calls\n(withCredentials)" --> B --> C
    C3 --> D
    C2 --> E
    A -.-> F
    C3 --> G
    C3 --> H
    C3 --> I

    style Client fill:#302b63,color:#fff,stroke:#6C63FF,stroke-width:2px
    style Edge fill:#1a1a2e,color:#fff,stroke:#6C63FF,stroke-width:2px
    style Server fill:#16213e,color:#fff,stroke:#6C63FF,stroke-width:2px
    style Data fill:#0f3460,color:#fff,stroke:#6C63FF,stroke-width:2px
    style External fill:#24243e,color:#fff,stroke:#6C63FF,stroke-width:2px
```

<br/>

## 🔄 Authentication Flow

```mermaid
sequenceDiagram
    participant U as User (Browser)
    participant F as Frontend (Vercel)
    participant B as Backend (Render)
    participant DB as MongoDB

    U->>F: Enter email + password
    F->>B: POST /api/auth/login (withCredentials)
    B->>DB: Find user by email
    DB-->>B: User document
    B->>B: bcrypt.compare(password)
    B->>B: Generate JWT
    B-->>F: Set-Cookie: token (HttpOnly, Secure, SameSite=None)
    F-->>U: Redirect to Dashboard
    U->>F: Navigate to protected route
    F->>B: GET /api/user/currentuser (cookie auto-sent)
    B->>B: Verify JWT from cookie
    B-->>F: 200 OK + user data
```

<br/>

## ✨ Key Features

<table>
<tr>
<td width="50%" valign="top">

### 👤 Authentication & Profile
- Signup/Login with bcrypt-hashed passwords
- JWT sessions via secure HTTP-only cookies
- Google Sign-In (Firebase Auth)
- OTP-based forgot/reset password via email
- Editable profile with Cloudinary avatar upload

### 🎓 Learning Experience
- Browse & search all published courses
- Rich course detail pages with curriculum preview
- Sequential lecture player for enrolled students
- Enrollment tracking per user
- Star-rating & written reviews per course
- **AI-powered course search** (Gemini API)

</td>
<td width="50%" valign="top">

### 🧑‍🏫 Educator Tools
- Role-based access — Educator-only routes
- Course creation → lecture creation → publish flow
- Edit/manage lectures within a course
- Personal dashboard of created courses

### 💳 Payments & Commerce
- Razorpay checkout integration
- Server-side payment verification
- Automatic enrollment on successful purchase

### 🛡️ Engineering
- CORS-secured cross-origin cookie auth
- Environment-based secret management
- Cloud DB (MongoDB Atlas) + Cloud media (Cloudinary)

</td>
</tr>
</table>

<br/>

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 19 · Vite · Redux Toolkit · React Router v7 · Tailwind CSS 4 |
| **Backend** | Node.js · Express.js |
| **Database** | MongoDB + Mongoose |
| **Auth** | JWT · bcryptjs · Firebase (Google OAuth) |
| **File Uploads** | Multer + Cloudinary |
| **Payments** | Razorpay |
| **Email** | Nodemailer (OTP delivery) |
| **AI** | Google Gemini API |
| **Hosting** | Vercel (Frontend) · Render (Backend) |

<br/>

## 📂 Project Structure

```
Virtual-Course/
├── backend/
│   ├── configs/          → DB, Cloudinary, Mail, Token setup
│   ├── controllers/      → auth, user, course, payment, ai, review logic
│   ├── middlewares/      → isAuth guard, Multer upload handler
│   ├── models/           → Mongoose schemas
│   ├── routes/           → Express route definitions
│   └── index.js          → Server entry point
│
└── frontend/
    ├── src/
    │   ├── pages/           → Login, SignUp, Dashboard, ViewCourse, etc.
    │   ├── pages/admin/      → Educator dashboard pages
    │   ├── components/       → Reusable UI components
    │   ├── customHooks/      → Data-fetching hooks
    │   ├── redux/             → Redux Toolkit slices
    │   └── App.jsx             → Root routes
    └── vercel.json              → SPA rewrite config
```

<br/>

## ⚙️ Environment Variables

**`backend/.env`**
```env
PORT=8000
MONGODB_URL=
JWT_SECRET=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
EMAIL=
EMAIL_PASS=
RAZORPAY_KEY_ID=
RAZORPAY_SECRET=
GEMINI_API_KEY=
```

**`frontend/.env`**
```env
VITE_API_URL=
```

> ⚠️ Never commit `.env` files — confirm they're listed in `.gitignore` before pushing.

<br/>

## 🚀 Getting Started

```bash
# 1. Clone
git clone https://github.com/Biswajitpa/Virtual-Course.git
cd Virtual-Course

# 2. Backend
cd backend
npm install
npm start

# 3. Frontend (in a new terminal)
cd frontend
npm install
npm run dev
```

Frontend runs at `http://localhost:5173`, connecting to backend at `http://localhost:8000`.

<br/>

## 🌐 Live Deployment

| Service | Platform | Purpose |
|---|---|---|
| Frontend | **Vercel** | React SPA hosting |
| Backend | **Render** | REST API server |
| Database | **MongoDB Atlas** | Persistent data storage |
| Media | **Cloudinary** | Avatar & course asset storage |

<br/>

## 🗺️ Roadmap

- [ ] Course completion certificates
- [ ] Resume-from-last-lecture progress tracking
- [ ] Discussion forum per course
- [ ] Wishlist & course bundles
- [ ] Multi-language support

<br/>

---

<div align="center">

## 👨‍💻 Developed By

<img src="https://github.com/Biswajitpa.png" width="100" style="border-radius:50%" />

### **Biswajit Pattanaik**

<a href="https://github.com/Biswajitpa"><img src="https://img.shields.io/badge/GitHub-Biswajitpa-181717?logo=github&style=for-the-badge" /></a>

<br/><br/>

⭐ **If this project helped or inspired you, consider giving it a star!** ⭐

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer)

</div>
