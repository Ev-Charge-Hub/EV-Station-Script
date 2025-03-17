## 🚀 EV-Charge-Hub Project with Docker Deployment

This project is designed to run the **EV-Charge-Hub** server using **Docker** and is prepared for future integration with a **Frontend** service. The deployment uses **Docker Compose** for streamlined management.

---

## ⚙️ Environment Variables (.env)
Create a `.env` file in the root directory based on `.env.example`.

**Example `.env` file:**
```
MONGO_URI=DB_URL
JWT_SECRET=JWT_SECRET
CLIENT_PORT=PORT_CLIENT
```

---

## 🐳 Docker Setup

### 🔥 Step 1: Build Docker Images
Run the following command to build the Docker images:

```bash
docker compose build
```

---

### 🟢 Step 2: Run the Services
To start the containers in the background:

```bash
docker compose up -d
```

To start the containers with logs in real-time:

```bash
docker compose up
```

---

### 🔍 Step 3: Verify the Running Services
To check running containers:

```bash
docker ps
```

To confirm that the server is running:

- API Endpoint: **`http://localhost:8080`**
- Frontend (future implementation): **`http://localhost:3000`**

---

### 🛑 Step 4: Stop the Services
```bash
docker compose down
```

---

## 🔐 Best Practices for Secrets Management
- **Never** commit your `.env` file to version control.
- Instead, use `envSimple` as a template for team members to configure their environment variables.

---

## 📦 Deployment to Docker Hub
**To push your image to Docker Hub:**

1. Build the image:
   ```bash
   docker build -t <username>/ev-charge-hub-server:V1.0 .
   ```

2. Tag the image:
   ```bash
   docker tag <username>/ev-charge-hub-server:V1.0 <username>/ev-charge-hub-server:latest
   ```

3. Push to Docker Hub:
   ```bash
   docker push <username>/ev-charge-hub-server:V1.0
   ```

---

## 📚 Future Enhancements
✅ Add Frontend Dockerfile for Next.js  
✅ Integrate CI/CD Pipeline for automatic deployment  
✅ Improve security with Docker secrets and environment control  

---