# Django Notes App

A 3-tier notes application with a Django backend, Nginx proxy, and MySQL database, all containerized using Docker.

## What It Does
This app lets you create, view, and manage notes. It features:
- A Django REST API (`api/`) for backend logic.
- A React frontend (`mynotes/`) for a slick user interface.
- MySQL (`db`) for persistent storage.

## My Contribution
I took an existing notes app and Dockerized it:
- Built a `Dockerfile` for the Django backend.
- Created a `docker-compose.yml` to orchestrate Django, Nginx, and MySQL.
- Configured Nginx (`nginx/default.conf`) as a reverse proxy to serve the app.
- Networked the services for seamless communication.

## How to Run
1. **Clone the repo**: Download the project from GitHub to your local machine.
   \`\`\`
   git clone https://github.com/Aaditya-Gupt/django-notes-app.git
   cd django-notes-app
   \`\`\`
2. **Set up environment variables**: Create a \`.env\` file with necessary settings (e.g., database credentials). Example:
   \`\`\`
   MYSQL_ROOT_PASSWORD=your_password_here
   \`\`\`
   Check \`.env.example\` (if provided) for required variables.
3. **Build and run**: Spin up the Docker containers.
   \`\`\`
   docker compose up --build
   \`\`\`
4. **Access the app**:
   - Frontend: Open \`http://localhost\` in your browser (served via Nginx).
   - API: Hit \`http://localhost:8000\` for the Django backend directly.
