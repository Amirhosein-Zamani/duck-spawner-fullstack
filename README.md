## Project Stack 🛠️

This project is a complete three-tier application setup using **Docker Compose** for easy, one-command deployment. It ensures optimized and lightweight container images through **Multi-Stage Builds**.

| Component | Technology | Directory | Notes |
| :--- | :--- | :--- | :--- |
| **Backend API** | Node.js / NestJS | `./duck-spawner-api` | Configured to connect to MongoDB via the Docker internal network. |
| **Frontend** | React / Yarn | `./duck-spawner-front` | Built and served using a lean **Multi-Stage Build** approach. |
| **Database** | MongoDB | N/A | Managed via a Docker Volume to ensure data persistence. |
## Quick Start Commands Cheat Sheet 🚀

| Action | Command | Purpose |
| :--- | :--- | :--- |
| **1. Initial Setup** | `docker compose up --build -d` | Builds the optimized Multi-Stage images and launches all services (API, Front, Mongo) in the background. |
| **2. Check Status** | `docker ps` | Lists all running containers to confirm services are Up. |
| **3. Access Frontend** | `http://localhost` | Access the application in your browser. |
| **4. Check Logs** | `docker compose logs -f` | View real-time logs for all services (press `Ctrl+C` to exit). |
| **5. Stop Containers** | `docker compose down` | Stops and removes all running containers and the network. |
| **6. Full Cleanup** | `docker compose down -v` | **Stops and deletes** containers, networks, **and the MongoDB data volume**. |
---
## 🖋️ Author

[Amirhossein Zamani](https://github.com/Amirhosein-Zamani)

---
