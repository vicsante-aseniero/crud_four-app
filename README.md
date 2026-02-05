# CRUD Four App

A full-stack CRUD application built with **Next.js 15** (TypeScript) for the front-end and **NestJS 11** (TypeScript) for the back-end API, containerized for development using VS Code DevContainers.

---

## 🏗️ Project Structure

```
crud-four-app/
├── api/                    # NestJS Backend API
│   ├── src/               # Application source code
│   ├── test/              # E2E tests
│   └── package.json       # API dependencies
├── ui/                     # Next.js Frontend UI
│   ├── app/               # App Router pages
│   ├── public/            # Static assets
│   └── package.json       # UI dependencies
├── .devcontainer/          # DevContainer configuration
│   ├── devcontainer.json  # Container settings
│   ├── docker-compose.yml # Docker services
│   └── Dockerfile         # Base image config
└── README.md              # This file
```

---

## 🛠️ Tech Stack

### Frontend (ui/)

| Technology  | Version  | Purpose                         |
| ----------- | -------- | ------------------------------- |
| Next.js     | 15.5.2   | React Framework with App Router |
| React       | 19.1.0   | UI Library                      |
| TypeScript  | ^5       | Type Safety                     |
| TailwindCSS | ^4       | Utility-First CSS               |
| Turbopack   | Built-in | Dev Server & Bundler            |

### Backend (api/)

| Technology | Version  | Purpose            |
| ---------- | -------- | ------------------ |
| NestJS     | 11.0.1   | Node.js Framework  |
| Express    | Platform | HTTP Server        |
| TypeScript | 5.7.3    | Type Safety        |
| Jest       | 30.0.0   | Unit & E2E Testing |
| Supertest  | 7.0.0    | HTTP Assertions    |

---

## 🚀 Quick Start

### Prerequisites

- Docker Desktop
- VS Code with [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Development Setup

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd crud-four-app
   ```

2. **Open in DevContainer**
   - Open project in VS Code
   - Press `F1` → "Dev Containers: Reopen in Container"
   - Wait for container to build (~3-5 minutes first time)

3. **Start the Backend API**

   ```bash
   cd api
   yarn install
   yarn start:dev
   ```

   API runs on: http://localhost:8000

4. **Start the Frontend UI**
   ```bash
   cd ui
   npm install
   npm run dev
   ```
   UI runs on: http://localhost:3000

---

## 📋 Available Scripts

### Backend API (`api/`)

| Command            | Description                      |
| ------------------ | -------------------------------- |
| `yarn start:dev`   | Start dev server with hot-reload |
| `yarn start:debug` | Start with debugger attached     |
| `yarn build`       | Build for production             |
| `yarn start:prod`  | Run production build             |
| `yarn test`        | Run unit tests                   |
| `yarn test:e2e`    | Run E2E tests                    |
| `yarn test:cov`    | Run tests with coverage          |
| `yarn lint`        | Lint and fix code                |
| `yarn format`      | Format code with Prettier        |

### Frontend UI (`ui/`)

| Command         | Description                  |
| --------------- | ---------------------------- |
| `npm run dev`   | Start dev server (Turbopack) |
| `npm run build` | Build for production         |
| `npm start`     | Run production server        |
| `npm run lint`  | Lint code                    |

---

## 🔌 Port Configuration

| Port  | Service    | Description                  |
| ----- | ---------- | ---------------------------- |
| 3000  | Next.js UI | Frontend application         |
| 8000  | NestJS API | Backend REST API             |
| 5432  | PostgreSQL | Database (via network)       |
| 6379  | Redis      | Cache (via network)          |
| 5672  | RabbitMQ   | Message broker (via network) |
| 15672 | RabbitMQ   | Management UI (via network)  |

---

## 🧪 Testing

### Unit Tests (Backend)

```bash
cd api
yarn test
```

### E2E Tests (Backend)

```bash
cd api
yarn test:e2e
```

### Test Coverage

```bash
cd api
yarn test:cov
```

---

## 🐳 DevContainer Features

The development container includes:

- **Node.js LTS** with npm, yarn, pnpm
- **NestJS CLI** for scaffolding
- **TailwindCSS CLI** standalone
- **Prisma ORM** tools
- **Testing**: Jest, Playwright, Cypress
- **API Tools**: Postman, REST Client
- **LocalStack** for AWS local development
- **Dapr CLI** for microservices
- **PostgreSQL Client** v13

### Resource Limits

- Memory: 8GB (limit) / 2GB (reserved)
- CPU: 2 cores (limit) / 1 core (reserved)

---

## 📚 Documentation

For detailed technical analysis, architecture patterns, and best practices, see:

- [**ANALYSIS.md**](./ANALYSIS.md) - In-depth technical documentation

---

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.
