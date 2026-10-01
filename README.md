# Node.js Demo App — CI/CD Pipeline with GitHub Actions

A simple Node.js web application with an automated CI/CD pipeline 
that tests, builds, and pushes a Docker image to Docker Hub on every 
push to `main`.

## Pipeline Proof
![GitHub Actions Status]<img width="1600" height="600" alt="githubaction" src="https://github.com/user-attachments/assets/a437ee5b-764a-4451-8a93-959309a172f9" />
![Docker Hub Image]<img width="1600" height="780" alt="hubdocker" src="https://github.com/user-attachments/assets/8a5dc4be-511b-4196-94a1-8a3e45e321e6" />


## What this does

1. **Test stage** — installs dependencies and runs a basic sanity test
2. **Build & Push stage** — builds a Docker image and pushes it to 
   Docker Hub, but only if the test stage passes

## Tech stack
- Node.js
- Docker
- GitHub Actions
- Docker Hub

## Pipeline file
See `.github/workflows/main.yml`

## Run locally
\`\`\`bash
npm install
npm start
\`\`\`

## Run with Docker
\`\`\`bash
docker build -t nodejs-demo-app .
docker run -p 3000:3000 nodejs-demo-app
\`\`\`

## Docker Hub image
`ShaikhAhmed41/nodejs-demo-app`
