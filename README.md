<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Poppins&size=32&duration=3000&pause=1000&color=000000&center=true&vCenter=true&width=600&lines=Virtual+Course;Learn+Anything%2C+Anywhere;Full+Stack+MERN+Platform" alt="Typing SVG animated banner" />

<br/>

![Banner](https://capsule-render.vercel.app/api?type=waving&color=0:000000,100:434343&height=180&section=header&text=VIRTUAL%20COURSES&fontSize=48&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=An%20Online%20Learning%20%26%20Course%20Selling%20Platform&descAlignY=58&descSize=18)

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

</div>

---

## 📖 About the Project

**Virtual Courses** is a full-stack **online learning and course-selling platform** where educators can create, publish, and sell courses, and students can browse, purchase, and learn through structured video lectures. The platform supports secure authentication, real-time payments, AI-assisted course search, and a dedicated educator dashboard to manage content — all wrapped in a clean, modern UI.

Built as a complete MERN-stack application, this project demonstrates real-world features like role-based access control, cloud media storage, payment gateway integration, and OTP-based password recovery — deployed end-to-end on production infrastructure.

---

## ✨ Key Features

### 👤 Authentication & User Management
- Secure Signup/Login with hashed passwords (bcrypt) and JWT-based sessions (HTTP-only cookies)
- Google Sign-In via Firebase Authentication
- OTP-based Forgot Password / Reset Password flow (email delivery)
- Editable user profiles with Cloudinary-hosted avatar uploads

### 🎓 Learning Experience
- Browse all published courses with search and category filters
- Detailed course view with curriculum, lecture list, and reviews
- Sequential lecture viewer for enrolled students
- Course enrollment tracking per user
- **AI-powered course search** to help students find the right course instantly
- Star-rating based review & feedback system for courses

### 🧑‍🏫 Educator Dashboard
- Role-based access — only users with an **Educator** role can create content
- Full course creation workflow: course details → lecture creation → publishing
- Add, edit, and manage lectures within a course
- Dashboard analytics for created courses and enrollments

### 💳 Payments
- Secure course purchases powered by **Razorpay**
- Order verification and enrollment activation on successful payment

### 🛡️ Security & Infrastructure
- CORS-protected REST API with credential-based cross-origin authentication
- Environment-based secret management for all API keys and credentials
- Cloud-hosted MongoDB Atlas database
- Media assets (avatars, thumbnails) stored and served via Cloudinary

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 19, Vite, Redux Toolkit, React Router v7, Tailwind CSS 4 |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (Mongoose ODM) |
| **Authentication** | JWT, bcryptjs, Firebase Auth (Google Sign-In) |
| **File Uploads** | Multer + Cloudinary |
| **Payments** | Razorpay |
| **Email/OTP** | Nodemailer |
| **AI Search** | Google Gemini API |
| **Deployment** | Vercel (Frontend) · Render (Backend) |

---

## 📂 Project Structure

```
Virtual-Course/
├── backend/
│   ├── configs/          # DB, Cloudinary, Mail, Token configs
│   ├── controllers/      # Route logic (auth, user, course, payment, ai, review)
│   ├── middlewares/      # Auth guard, Multer file handling
│   ├── models/           # Mongoose schemas
│   ├── routes/           # Express route definitions
│   └── index.js          # Server entry point
│
└── frontend/
    ├── src/
    │   ├── pages/         # Route-level pages (Login, SignUp, Dashboard, etc.)
    │   ├── pages/admin/    # Educator dashboard pages
    │   ├── components/     # Reusable UI components
    │   ├── customHooks/    # Data-fetching hooks
    │   ├── redux/          # Redux Toolkit slices
    │   └── App.jsx          # Root component & route definitions
    └── vercel.json          # SPA routing config
```

---

## ⚙️ Environment Variables

**Backend `.env`**
```
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

**Frontend `.env`**
```
VITE_API_URL=
```

> ⚠️ Never commit `.env` files. Ensure they are listed in `.gitignore`.

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Biswajitpa/Virtual-Course.git
cd Virtual-Course
```

### 2. Setup Backend
```bash
cd backend
npm install
npm start
```

### 3. Setup Frontend
```bash
cd frontend
npm install
npm run dev
```

The app will be available at `http://localhost:5173`, connecting to the backend at `http://localhost:8000`.

---

## 🌐 Deployment

| Service | Platform |
|---|---|
| Frontend | [Vercel](https://vercel.com) |
| Backend | [Render](https://render.com) |
| Database | MongoDB Atlas |
| Media Storage | Cloudinary |

---

## 🗺️ Roadmap

- [ ] Live doubt-solving / discussion forums
- [ ] Certificate generation on course completion
- [ ] Course progress tracking with resume-from-last-lecture
- [ ] Wishlist & course bundles
- [ ] Multi-language support

---

<div align="center">

## 👨‍💻 Developed By

### **Biswajit Pattanaik**

<a href="https://github.com/Biswajitpa">
  <img src="https://img.shields.io/badge/GitHub-Biswajitpa-181717?logo=github&style=for-the-badge" />
</a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:434343,100:000000&height=100&section=footer" />

⭐ If you found this project interesting, consider giving it a star on GitHub!

</div>
