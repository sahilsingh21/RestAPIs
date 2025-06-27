Below is a tailored and structured `README.md` that covers **two separate projects** in the same repository: one MERN REST API and one Go-based Student API. It includes all essential sections—overview, setup, usage, endpoints, config, tests, roadmap, and contribution guidelines.

---

```markdown
# 🎯 RestAPIs

*Two REST API projects in one repo:*

1. **MERN REST API** – Node.js + Express + MongoDB  
2. **Student API** – GoLang-based student management API

---

## 📋 Table of Contents
- [Overview](#overview)
- [🚀 Projects](#projects)
  - [1. MERN REST API](#1-mern-rest-api)
  - [2. Student API (Go)](#2-student-api-go)
- [📦 Installation](#installation)
- [⚙️ Configuration](#configuration)
- [🧪 Testing](#testing)
- [📈 Roadmap](#roadmap)
- [🤝 Contributing](#contributing)
- [📄 License](#license)

---

## 📋 Overview
This repository hosts two independent API projects:

- A **MERN REST API** structured for CRUD operations with clean routing.
- A **GoLang Student API** (`student-api/`), built to manage student records (likely using frameworks like Gin/Gorm) :contentReference[oaicite:1]{index=1}.

---

## 🚀 Projects

### 1. MERN REST API
Location: root directory

**Tech stack:** Node.js, Express, MongoDB (via Mongoose)

**Features:**
- Standard RESTful routes (GET, POST, PUT, DELETE)
- Middleware for validation & error handling
- Modular architecture with dedicated folders for `controllers`, `models`, `routes`, and `middleware`

**Endpoints (example):**
```

GET    /api/items
POST   /api/items
GET    /api/items/\:id
PUT    /api/items/\:id
DELETE /api/items/\:id

````

---

### 2. Student API (Go)
Location: `student-api/` folder

**Tech stack:** GoLang, likely with Gin + Gorm, possibly Redis/MySQL :contentReference[oaicite:2]{index=2}

**Features:**
- CRUD for student entities
- Database-backed storage (MySQL) with ORM
- Optional caching layer (Redis)
- Clean project layout per Go best practices :contentReference[oaicite:3]{index=3}

---

## 📦 Installation

### Prerequisites
- **Node.js** (v14+), npm  
- **MongoDB**
- **Go** (v1.18+)  
- (Optional) **Redis** and **MySQL**

### Setup

```bash
git clone https://github.com/sahilsingh21/RestAPIs.git
cd RestAPIs
````

#### MERN API

```bash
cd .
npm install
```

#### Go Student API

```bash
cd student-api
go mod download
```

---

## ⚙️ Configuration

Create `.env` files in each project as needed.

### MERN (.env)

```
PORT=3000
MONGO_URI=mongodb://localhost:27017/restapis
JWT_SECRET=your_jwt_secret
```

### Go Student API (`student-api/.env`)

```
PORT=8080
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASS=secret
DB_NAME=students_db
REDIS_ADDR=localhost:6379  # optional
```

---

## 🚀 Usage

### Run MERN API

```bash
cd RestAPIs
npm start          # or npm run dev with nodemon
```

Access at `http://localhost:3000/api/...`

### Run Go Student API

```bash
cd student-api
go run main.go -config config/local.yaml
```

Access at `http://localhost:8080/...`
(e.g., `GET /students`, `POST /students`, etc.)

---

## 🧪 Testing

If unit tests exist:

### MERN

```bash
npm test
```

### Go Student API

```bash
cd student-api
go test ./...
```

---

## 📈 Roadmap

### MERN

* Add authentication (JWT)
* Pagination & filtering
* Add API documentation (Swagger/OpenAPI)

### Go Student API

* Implement auth middleware
* Add validation & structured docs
* Dockerize with MySQL/Redis containers

---

## 🤝 Contributing

1. Fork and clone the repo
2. Create a branch:

   * `feature/mern-...` or `feature/go-...`
3. Commit work with meaningful messages
4. Push branch and open a PR
5. Run tests and ensure style consistency


