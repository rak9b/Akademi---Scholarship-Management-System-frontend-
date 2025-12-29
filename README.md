# Akademi – Elite Scholarship Management System [Signature Edition]
![Scholarship System Banner](https://images.unsplash.com/photo-1523050335392-93851179424c?auto=format&fit=crop&q=80&w=1600)

> **Institutional Excellence. Global Connectivity. Precision Academia.**

[![Live Demo](https://img.shields.io/badge/Demo-Live-brightgreen)](https://akademi---scholarship-management-system-frontend-.vercel.app)
[![Build Status](https://img.shields.io/badge/Build-Passing-success)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

Akademi is a world-class Scholarship Management Platform designed to harmonize global educational opportunities with high-achieving candidates. Reimagined with a **Signature Edition** aesthetic, it provides an elite registry for students, advanced oversight for moderators, and precision analytics for administrators.

---

## 🏛️ PROJECT OVERVIEW & IDENTITY

Akademi serves as the central nervous system for institutional scholarship logistics. It addresses the fragmented landscape of academic grants by providing a verified, high-contrast, and ultra-responsive registry.

- **Tagline**: Bridge the gap to global excellence
- **Live Demo**: [Registry Portal](https://akademi---scholarship-management-system-frontend-.vercel.app)
- **Backend API**: [Intelligence Layer](https://akademi-scholarship-management-syst-beta.vercel.app)
- **Status**: Production Ready / Signature V2.5
- **Mission**: Academic Opportunities & Institutional Integrity

---

## ✅ FEATURES & COMPLETE PAGE REGISTRY

### **🌍 Public Pages**
| Page | Route | Description |
|:-----|:------|:------------|
| **Home** | `/` | Elite landing page with staggered reveals, scholarship showcase, testimonials |
| **All Scholarships** | `/all-scholarships` | Comprehensive registry with advanced filtering, sorting by fees |
| **Scholarship Details** | `/scholarship-details/:id` | Individual dossier with reviews, descriptions, application gateway |
| **About Us** | `/about` | Mission, vision, institutional values |
| **Blog** | `/blog` | Educational insights and scholarship guides |
| **Resources** | `/resources` | Downloadable materials and academic toolkits |
| **Contact** | `/contact` | Interactive contact form with map integration |
| **Pricing** | `/pricing` | Service tiers and payment structures |
| **Login** | `/login` | Secure authentication portal |
| **Register** | `/register` | Multi-field registration with role selection |
| **404 Not Found** | `*` | Custom error page |

### **📊 Dashboard Pages (Role-Based Access)**

#### **Student/Candidate Dashboard**
| Page | Route | Features |
|:-----|:------|:---------|
| **Profile** | `/dashboard/profile` | Personal information management |
| **My Applications** | `/dashboard/my-application/:id` | Application tracking, status updates, fee payment |
| **My Reviews** | `/dashboard/my-reviews/:id` | Submitted reviews management, edit/delete capabilities |

#### **Moderator Dashboard**
| Page | Route | Features |
|:-----|:------|:---------|
| **Add Scholarship** | `/dashboard/add-scholarships` | Create new scholarship entries with image upload |
| **Manage Scholarships** | `/dashboard/manage-scholarships` | Edit/delete institutional offerings |
| **Manage Applications** | `/dashboard/manage-applications` | Review applications, provide feedback, approve/reject |
| **Manage Reviews** | `/dashboard/manage-reviews` | Monitor and moderate user feedback |

#### **Admin Dashboard**
| Page | Route | Features |
|:-----|:------|:---------|
| **Analytics** | `/dashboard/analytics` | Obsidian Laboratory - real-time metrics, charts (Bar, Pie, Area) |
| **Manage Users** | `/dashboard/manage-users` | User registry, role assignment, account deletion |
| **All Features** | *Inherits all Moderator capabilities* | Full system access |

---

## 💻 TECHNOLOGY STACK

| Layer | Technologies |
| :--- | :--- |
| **Frontend** | React 18.3, Vite 6.0, Framer Motion 11 |
| **Styling** | Tailwind CSS 3.4, DaisyUI, Custom CSS Variables |
| **State/Data** | @tanstack/react-query (v5), Axios, Context API |
| **Forms** | React Hook Form, Zod Validation |
| **Backend** | Node.js 20+, Express.js 4.21 |
| **Database** | MongoDB Atlas (Cluster Intelligence) |
| **Authentication** | Firebase Auth, JWT |
| **Payments** | Stripe (Secure Transaction Layer) |
| **Deployment** | Vercel (Frontend + Backend), MongoDB Atlas |

---

## 📂 PROJECT STRUCTURE

```text
akademi-root/
├── client/                          # Elite UI Engine
│   ├── src/
│   │   ├── Components/              # Reusable UI Modules
│   │   ├── Context/                 # AuthProvider, State Management
│   │   │   ├── AuthProvider.jsx
│   │   │   ├── PrivateRoute.jsx
│   │   │   ├── AdminRoute.jsx
│   │   │   └── AuthorizedRoute.jsx
│   │   ├── Hooks/                   # Custom Hooks
│   │   │   ├── useRole.jsx
│   │   │   └── OtherPageBanner.jsx
│   │   ├── Pages/                   # All Application Pages
│   │   │   ├── HomePage/            # Home Page Components
│   │   │   │   ├── Home.jsx
│   │   │   │   ├── Banner.jsx
│   │   │   │   ├── TopScholarships.jsx
│   │   │   │   ├── ScholarshipCard.jsx
│   │   │   │   ├── FeaturesSection.jsx
│   │   │   │   ├── TestimonialsSection.jsx
│   │   │   │   ├── Reviews.jsx
│   │   │   │   ├── HowItWorks.jsx
│   │   │   │   ├── Contact.jsx
│   │   │   │   ├── LatestBlogs.jsx
│   │   │   │   ├── NewsLetter.jsx
│   │   │   │   └── FAQ.jsx
│   │   │   ├── AllScholarshipsPage/
│   │   │   │   └── AllScholarships.jsx
│   │   │   ├── ScholarshipsDetails/
│   │   │   │   ├── ScholarshipsDetails.jsx
│   │   │   │   ├── Description.jsx
│   │   │   │   └── Review.jsx
│   │   │   ├── Dashboard/
│   │   │   │   ├── Dashboard.jsx
│   │   │   │   ├── Admin/
│   │   │   │   │   ├── AdminDashboard.jsx
│   │   │   │   │   ├── Profile.jsx
│   │   │   │   │   ├── AddScholarships.jsx
│   │   │   │   │   ├── ManageScholarships.jsx
│   │   │   │   │   ├── ManageApplications.jsx
│   │   │   │   │   ├── ManageReviews.jsx
│   │   │   │   │   ├── AllUser.jsx
│   │   │   │   │   └── Charts.jsx
│   │   │   │   ├── User/
│   │   │   │   │   ├── User.jsx
│   │   │   │   │   ├── MyApplication.jsx
│   │   │   │   │   └── MyReviews.jsx
│   │   │   │   └── Moderator/
│   │   │   │       └── Moderator.jsx
│   │   │   ├── Login/
│   │   │   │   └── Login.jsx
│   │   │   ├── Register/
│   │   │   │   └── Register.jsx
│   │   │   ├── AboutUs/
│   │   │   │   └── AboutUs.jsx
│   │   │   ├── Blog/
│   │   │   │   └── Blog.jsx
│   │   │   ├── Resources/
│   │   │   │   └── Resources.jsx
│   │   │   ├── ContactUs/
│   │   │   │   ├── Contact.jsx
│   │   │   │   └── Map.jsx
│   │   │   ├── Pricing/
│   │   │   │   └── Pricing.jsx
│   │   │   ├── PaymentGateway/
│   │   │   │   └── PaymentForm.jsx
│   │   │   └── NotFound.jsx
│   │   ├── Layout/
│   │   │   └── Root.jsx
│   │   ├── main.jsx                 # Router Configuration
│   │   └── index.css                # Global Styles
│   ├── tailwind.config.js
│   ├── vite.config.js
│   └── package.json
└── server/                          # Hardened API Registry
    ├── index.js                     # Core Routing & Intelligence
    ├── .env                         # Security Parameters
    └── seed-v2.js                   # Demographic Data Initialization
```

---

## 🚀 SETUP & INSTALLATION

### **Prerequisites**
- Node.js 20+ 
- npm or yarn
- Git
- MongoDB Atlas account
- Stripe account (for payments)

### **1. Clone the Repository**
```bash
git clone https://github.com/rak9b/Akademi---Scholarship-Management-System-frontend-.git
cd Akademi
```

### **2. Environment Configuration**

**Server `.env`:**
```env
PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/akademi
STRIPE_SECRET_KEY=sk_test_...
```

**Client `.env`:**
```env
VITE_API_URL=http://localhost:5000
VITE_STRIPE_PUBLIC_KEY=pk_test_...
VITE_FIREBASE_API_KEY=...
VITE_FIREBASE_AUTH_DOMAIN=...
VITE_FIREBASE_PROJECT_ID=...
```

### **3. Installation & Launch**
```bash
# Install dependencies
npm install

# Development mode
npm run dev

# Production build
npm run build
```

---

## 🔐 TESTING CREDENTIALS

| Role | Email | Password | Dashboard Access |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin@signature.com` | `Signature@2025` | Full System Access + Analytics |
| **Moderator**| `mod@registry.org` | `Registry@2025` | Content Management |
| **Student**| `student@global.edu`| `Student@2025` | Applications & Reviews |

---

## 🏗️ SYSTEM ARCHITECTURE DIAGRAMS

### **High-Level System Flow**
```mermaid
graph TD
    A[User Browser] -->|HTTPS| B[Vercel CDN]
    B --> C{Authentication}
    C -->|Valid Token| D[React App]
    C -->|Invalid| E[Login Page]
    D --> F[TanStack Query]
    F -->|API Calls| G[Express Backend]
    G --> H[(MongoDB Atlas)]
    G --> I[Stripe API]
    D --> J[Firebase Auth]
```

### **Authentication Flow**
```mermaid
sequenceDiagram
    participant U as User
    participant F as Frontend
    participant FB as Firebase
    participant BE as Backend
    participant DB as MongoDB

    U->>F: Enter Credentials
    F->>FB: Authenticate
    FB->>F: Return JWT Token
    F->>BE: Request with JWT
    BE->>BE: Verify Token
    BE->>DB: Fetch User Data
    DB->>BE: User Profile
    BE->>F: Authorized Response
    F->>U: Dashboard Access
```

### **Application Submission Flow**
```mermaid
graph LR
    A[Browse Scholarships] --> B[View Details]
    B --> C[Click Apply]
    C --> D{User Logged In?}
    D -->|No| E[Redirect to Login]
    D -->|Yes| F[Fill Application]
    F --> G[Upload Documents]
    G --> H[Payment Page - Stripe]
    H --> I[Process Payment]
    I --> J[Submit to Database]
    J --> K[Email Confirmation]
    K --> L[Dashboard Tracking]
```

### **Admin Analytics Data Flow**
```mermaid
graph TD
    A[Admin Dashboard] --> B[Charts Component]
    B --> C[TanStack Query]
    C --> D[API: /all-collections-data]
    D --> E[MongoDB Aggregation]
    E --> F[Scholarships Collection]
    E --> G[Users Collection]
    E --> H[Applications Collection]
    E --> I[Reviews Collection]
    F & G & H & I --> J[Aggregate Data]
    J --> K[Return JSON]
    K --> L[Recharts Visualization]
    L --> M[Bar/Pie/Area Charts]
```

### **Role-Based Access Control (RBAC)**
```mermaid
graph TD
    A[User Login] --> B{Check Role}
    B -->|Student| C[Student Dashboard]
    B -->|Moderator| D[Moderator Panel]
    B -->|Admin| E[Admin Suite]
    
    C --> F[My Applications]
    C --> G[My Reviews]
    C --> H[Profile]
    
    D --> I[Add Scholarships]
    D --> J[Manage Applications]
    D --> K[Manage Reviews]
    D --> F
    D --> G
    D --> H
    
    E --> L[Analytics]
    E --> M[User Management]
    E --> I
    E --> J
    E --> K
    E --> F
    E --> G
    E --> H
```

### **Database Schema Architecture**
```mermaid
erDiagram
    USERS ||--o{ APPLICATIONS : submits
    USERS ||--o{ REVIEWS : writes
    SCHOLARSHIPS ||--o{ APPLICATIONS : receives
    SCHOLARSHIPS ||--o{ REVIEWS : has
    
    USERS {
        string _id
        string name
        string email
        string role
        string photoURL
        date createdAt
    }
    
    SCHOLARSHIPS {
        string _id
        string scholarshipName
        string universityName
        string universityImage
        string scholarshipCategory
        number applicationFees
        number serviceCharge
        date applicationDeadline
        string subjectCategory
        string degree
    }
    
    APPLICATIONS {
        string _id
        string userId
        string scholarshipId
        string status
        string feedback
        date appliedDate
        boolean paymentStatus
    }
    
    REVIEWS {
        string _id
        string userId
        string scholarshipId
        number rating
        string comment
        date reviewDate
    }
```

---

## 🎨 DESIGN SYSTEM

### **Color Palette**
- **Primary Green**: `#16a34a` (Deep Emerald)
- **Dark**: `#000000` (Obsidian)
- **Light**: `#FDFDFC` (Ivory)
- **Accent**: `#185137` (Dark Green)

### **Typography**
- **Body**: Inter (Technical Precision)
- **Headings**: Bricolage Grotesque (Institutional Authority)
- **Monospace**: JetBrains Mono (Code Display)

### **UI Philosophy**
- Glassmorphism with backdrop-blur effects
- High-contrast institutional hierarchy
- Staggered reveal animations (Framer Motion)
- Micro-interactions on all interactive elements

---

## 🛠️ TESTING STRATEGY

- **Lint Status**: ✅ 0 errors, 0 warnings
- **Build Status**: ✅ Exit Code 0
- **Unit Testing**: Jest & Vitest (business logic validation)
- **E2E Testing**: Playwright (user flow simulation)
- **Security**: npm audit, Snyk dependency scanning

---

## 🛡️ SECURITY CONSIDERATIONS

- **Password Hashing**: Bcrypt (12 salt rounds)
- **JWT Tokens**: 24h expiration, HttpOnly cookies
- **Input Validation**: Zod schemas on all endpoints
- **XSS Protection**: DOMPurify for user-generated content
- **CORS**: Configured for production domains only
- **Rate Limiting**: API throttling on sensitive endpoints

---

## 📊 MONITORING & LOGGING

- **Health Endpoint**: `/health` (uptime verification)
- **Diagnostics**: `/diag` (system status)
- **Error Tracking**: Winston logging integration
- **Performance**: Vercel Analytics (Core Web Vitals)
- **Database**: MongoDB Atlas monitoring

---

## 🚀 DEPLOYMENT

### **Frontend (Vercel)**
```bash
vercel --prod
```

### **Backend (Vercel)**
```bash
cd server
vercel --prod
```

### **Environment Variables** (Vercel Dashboard)
- `MONGODB_URI`
- `STRIPE_SECRET_KEY`
- `JWT_SECRET`

---

## 📈 API ENDPOINTS

### **Public Routes**
- `GET /` - Fetch top scholarships
- `GET /scholarship/:id` - Get scholarship details
- `GET /all-scholarships` - Get all scholarships with filters
- `GET /health` - Health check

### **Protected Routes**
- `POST /apply` - Submit application
- `POST /review` - Submit review
- `GET /my-applications/:email` - User's applications
- `GET /my-reviews/:email` - User's reviews

### **Admin/Moderator Routes**
- `POST /add-scholarship` - Create scholarship
- `PUT /scholarship/:id` - Update scholarship
- `DELETE /scholarship/:id` - Delete scholarship
- `GET /all-collections-data` - Analytics data
- `PATCH /application-status/:id` - Update application status

---

## 🏆 ROADMAP & FUTURE ENHANCEMENTS

- [ ] AI-Powered Scholarship Matching
- [ ] Multi-lingual Support (10+ languages)
- [ ] Mobile-native PWA
- [ ] Real-time Notifications (WebSocket)
- [ ] Advanced Analytics (ML insights)
- [ ] Blockchain Verification System

---

## 📝 LICENSE

MIT License - See [LICENSE](LICENSE) file for details

---

## 🤝 CONTRIBUTING

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

---

## 📞 SUPPORT & CONTACT

- **Issues**: [GitHub Issues](https://github.com/rak9b/Akademi---Scholarship-Management-System-frontend-/issues)
- **Email**: support@akademi.edu
- **Documentation**: [Full Docs](https://akademi-docs.vercel.app)

---

**© 2025 Akademi Institutional Systems | Elite. Secured. Production-Ready.**

![Footer](https://img.shields.io/badge/Built%20with-React%20%7C%20Node.js%20%7C%20MongoDB-brightgreen)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success)
