# 🤖 AI Multi-Agent Project Manager

### An AI-Powered Platform for Intelligent Project Planning, Task Management, and Team Collaboration

An intelligent project management platform designed to simplify project planning, task allocation, progress tracking, and team coordination using a web-based interface and a multi-agent AI architecture.

The system provides dedicated Admin and Agent dashboards, centralized project management, task tracking, and an architecture for AI-assisted project planning and review.

---

## 📌 Overview

The **AI Multi-Agent Project Manager** is a web application designed to help teams organize projects, manage tasks, coordinate team members, and monitor project progress through a centralized platform.

Traditional project management often requires manual task creation, task assignment, progress monitoring, and status reporting. This can make project coordination time-consuming and make it harder to identify potential delays.

This project combines conventional project management functionality with a multi-agent AI approach to support intelligent planning, execution monitoring, and project review.

The application provides role-based access for administrators and agents, project and task management, project workspaces, and dashboards for tracking work.

The AI architecture can organize responsibilities among specialized agents, including a Planner Agent, Executor Agent, and Reviewer Agent. Their actual capabilities depend on the AI workflows implemented and enabled in the application.

## 🎯 Problem Statement

Project teams often face difficulties in planning projects, distributing tasks, monitoring progress, identifying delays, and maintaining coordination among team members.

Manual management can lead to inefficient task allocation, limited visibility into project health, and delayed identification of potential problems.

## 💡 Proposed Solution

The AI Multi-Agent Project Manager provides a centralized platform for managing projects and coordinating team activities.

It combines project management functionality with AI-assisted workflows to help teams organize tasks, analyze project progress, and obtain useful recommendations.

The goal is to reduce repetitive project management work and improve visibility, coordination, and decision-making.

## ✨ Key Features

### 1. Role-Based Authentication
- Separate Admin and Agent access.
- Role-specific dashboards.
- Access to relevant project management functionality.

### 2. Project Management
- Create new projects.
- Enter project titles, descriptions, dates, and statuses.
- View project information.
- Edit project details.
- Delete projects when appropriate.

### 3. Task Management
- Create tasks for individual projects.
- Assign tasks to team members.
- Set task priorities.
- Track task status.
- Organize tasks by project.

### 4. Admin Dashboard
- View and manage projects.
- Create and organize tasks.
- Monitor project information.
- Access project details and team task information.

### 5. Agent Dashboard
- View assigned work.
- Access project workspaces.
- Track task progress.
- Update task statuses where permitted.
- Identify pending, in-progress, and completed tasks.

### 6. Multi-Agent AI Architecture

The application is designed around specialized AI agents with distinct responsibilities.

**Planner Agent**
- Supports project planning.
- Helps organize project requirements.
- Supports task breakdown and planning when the corresponding AI workflow is implemented.

**Executor Agent**
- Supports task execution workflows.
- Helps monitor task progress and execution information when connected to the relevant application tools.

**Reviewer Agent**
- Supports project review.
- Can analyze available project information and generate recommendations when the review workflow is implemented.

The agents can work together to support a more intelligent project management process.

### 7. Project Workspace
- View project-specific information.
- Access tasks associated with a project.
- Monitor task completion.
- Review task assignments and priorities.

### 8. Progress Monitoring
- Display task statuses.
- Track completed and pending work.
- View project-level task summaries.
- Support progress review through dashboards.

### 9. REST API Integration
- Connect the frontend with backend services.
- Exchange project and task information.
- Support application operations through API endpoints.

---

## 🧠 Multi-Agent Architecture

The system is organized around a project management workflow supported by specialized AI agents.

```text
                  USER
                   |
                   v
          AI PROJECT MANAGER
                   |
          +--------+--------+
          |        |        |
          v        v        v
       PLANNER  EXECUTOR  REVIEWER
        AGENT    AGENT     AGENT
          |        |        |
          v        v        v
       Planning  Execution  Review
       & Tasks   Monitoring & Insights
          |        |        |
          +--------+--------+
                   |
                   v
          PROJECT MANAGEMENT
              APPLICATION
                   |
          +--------+--------+
          |                 |
          v                 v
      Backend API        Database
```

**Architecture responsibilities:**

- **Planner Agent:** Supports project planning and task organization.
- **Executor Agent:** Supports execution-related workflows and progress monitoring.
- **Reviewer Agent:** Supports project analysis and review.
- **Backend:** Processes application requests and manages project and task operations.
- **Database:** Stores application information.

*Note: This diagram represents the intended logical architecture. The actual agent-to-agent communication and tool integrations should match the implementation in the repository.*

---

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | React |
| Styling | Tailwind CSS |
| Backend | Node.js |
| Backend Framework | Express.js |
| Database | MySQL |
| Frontend-Backend Communication | Axios |
| API Architecture | REST APIs |
| AI Components | Multi-agent AI architecture |
| Development Environment | Node.js, npm, and Visual Studio Code |
| Version Control | Git and GitHub |

**Important:** Confirm the AI provider, model, orchestration framework, and any additional libraries against your actual dependency files before listing them as implemented technologies.

---

## 🏗️ Project Structure

The following is a representative structure for the application. Adjust the file and directory names to match your actual repository.

```text
AI-MultiAgent-Project-Manager/
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── index.html
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── services/
│   ├── config/
│   ├── middleware/
│   ├── server.js
│   └── package.json
│
├── ai-agents/
│   ├── planner-agent/
│   ├── executor-agent/
│   └── reviewer-agent/
│
├── database/
│   └── schema.sql
│
├── .gitignore
├── .env.example
└── README.md
```

*This structure is illustrative. Keep only directories and files that actually exist in your project.*

---

## ⚙️ Getting Started

### Prerequisites

Install the following tools before running the application:

- Node.js
- npm
- MySQL Server
- Git
- A code editor such as Visual Studio Code

If your AI functionality uses an external model provider, configure its required credentials as described in your project's environment configuration.

### 1. Clone the Repository

Replace the example repository URL with your actual GitHub repository URL.

```bash
git clone https://github.com/YOUR_USERNAME/AI-MultiAgent-Project-Manager.git
cd AI-MultiAgent-Project-Manager
```

### 2. Set Up the Frontend

Open a terminal and navigate to the frontend directory:

```bash
cd frontend
npm install
```

Create the frontend environment configuration if your application requires one.

For example, if the frontend uses an environment variable for the backend API:

```env
VITE_API_BASE_URL=http://localhost:5000
```

Use the actual variable name expected by your frontend code.

Start the development server:

```bash
npm run dev
```

Open the local URL displayed in your terminal.

### 3. Set Up the Backend

Open another terminal from the project root:

```bash
cd backend
npm install
```

Configure the backend environment variables according to your application.

Example:

```env
PORT=5000
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=ai_project_manager
```

These are example variable names. Use the exact names expected by your backend configuration.

### 4. Configure MySQL

Start your MySQL server and create the database.

```sql
CREATE DATABASE ai_project_manager;
```

Import your project's database schema or run its database initialization procedure.

For example, if the repository contains `database/schema.sql`, execute the appropriate import command:

```bash
mysql -u your_mysql_username -p ai_project_manager < ../database/schema.sql
```

Update the database connection settings in your environment configuration.

**Note:** The import command assumes that the schema file exists at the specified location. Change the path if your project uses a different structure.

### 5. Configure AI Integration

If your application uses an external LLM provider, add the required API key and model configuration to the backend environment.

Example:

```env
LLM_API_KEY=your_api_key
LLM_MODEL=your_configured_model
```

These are illustrative variable names, not guaranteed configuration keys for your implementation.

Never commit API keys, passwords, or private environment files to GitHub.

If your agents use a local model or a different configuration mechanism, follow the corresponding setup instructions.

### 6. Start the Backend

From the backend directory, run the start command defined in its `package.json`.

For example, if the project defines a `start` script:

```bash
npm start
```

If it defines a development script:

```bash
npm run dev
```

The backend should start on the configured port.

For the example configuration, the address would be:

```text
http://localhost:5000
```

The actual address depends on your server configuration.

### 7. Run the Application

Ensure that:
- MySQL is running.
- The database is configured correctly.
- The backend server is running.
- The frontend points to the correct backend API.
- Required AI services are configured.

Open the frontend in your browser and sign in using an account configured for your application.

---

## 🔄 Application Workflow

The typical project management workflow is:

1. The user signs in through the application.
2. The user accesses the appropriate Admin or Agent dashboard.
3. The administrator creates or selects a project.
4. Tasks are created and associated with projects.
5. Tasks are assigned to team members with appropriate priorities.
6. Agents access their assigned projects and tasks.
7. Task statuses are updated as work progresses.
8. Project information is displayed through the dashboard.
9. Where implemented, AI agents support planning, execution monitoring, and project review.

The exact workflow depends on the features and permissions enabled in the deployed application.

---

## 📊 Task Status Management

Tasks can be organized according to their current status.

| Status | Description |
|---|---|
| Pending | The task has not yet started. |
| In Progress | The task is currently being worked on. |
| Completed | The task has been completed. |

Task priorities help distinguish work according to its importance.

The available priority levels and permitted status transitions should match the application's implementation.

---

## 🤖 AI Capabilities

The multi-agent approach separates project-related responsibilities into specialized workflows.

### Planner Agent
Supports planning and task organization.

### Executor Agent
Supports task execution and progress-related workflows.

### Reviewer Agent
Supports reviewing project information and identifying possible improvements.

When connected to an LLM and application tools, these agents can support natural-language project assistance and AI-assisted decision-making.

For a fully implemented AI workflow, the system should demonstrate actual AI-generated results rather than relying only on predefined responses or static dashboard information.

---

## 🔐 Security and Data Handling

Security is important because the application manages project information and team assignments.

Recommended practices include:

- Store passwords securely using an appropriate password-hashing method.
- Validate user input on the backend.
- Use parameterized database queries or a suitable ORM.
- Protect restricted routes with server-side authorization.
- Store credentials and API keys in environment variables.
- Avoid exposing secrets in frontend code.
- Apply appropriate permissions to project and task operations.
- Do not commit `.env` files containing sensitive credentials.

Document and verify the security controls that are actually implemented before describing them as completed features.

---

## 🧪 Testing and Validation

Before deploying the application, verify the following:

- User authentication and role-based access.
- Project creation, editing, and deletion.
- Task creation and assignment.
- Task status updates.
- MySQL connectivity and data persistence.
- Frontend-backend API communication.
- Error handling for invalid requests.
- AI agent behavior and model connectivity, if applicable.
- Correct handling of incomplete or failed AI responses.
- Dashboard consistency with stored project and task data.

Run the test commands supported by your repository's `package.json` files.

For example:

```bash
npm test
```

This command is applicable only if a test script is configured.

---

## 🚀 Future Enhancements

Potential enhancements include:

- AI-assisted project planning.
- Intelligent task prioritization.
- Project risk analysis.
- Automated project summaries.
- Improved team workload analysis.
- Natural-language project queries.
- Project-document retrieval using RAG.
- AI tool integration using MCP where appropriate.
- Notifications for important project events.
- Enhanced analytics and reporting.
- Deployment and scalability improvements.

These are potential extensions, not claims that every feature is already implemented.

---

## 🌍 Real-World Applications

The platform can support project coordination in:

- Software development teams.
- Student project groups.
- Academic and research projects.
- Startup teams.
- Collaborative engineering projects.
- Organizations managing multiple projects.

Its usefulness depends on the quality of the implemented project management and AI workflows.

---

## 🏆 Hackathon Track

**INNOVA X 2K26 — Open Innovation: AI For The Future**

The project addresses a real-world challenge: making project planning, coordination, and progress review more efficient.

By combining project management functionality with a multi-agent AI approach, the platform aims to help teams organize work, improve project visibility, and support informed decisions.

The innovation should be demonstrated through working AI functionality, measurable outcomes where possible, and a clear explanation of how the agents contribute beyond conventional project management features.

---

## 👩‍💻 Author

**Rithi R**

B.Tech. — Artificial Intelligence and Data Science  
KPR Institute of Engineering and Technology  
Coimbatore, Tamil Nadu, India

GitHub: [Rithirajendran](https://github.com/Rithirajendran)

LinkedIn: [Rithi R](https://www.linkedin.com/in/rithi-r-011264380)

Portfolio: [Personal Portfolio](https://rithirajendran.github.io/portfolio/)

---

## 📄 License

Choose an appropriate open-source license if you intend to distribute this project publicly.

Until a license is added to the repository, reuse and redistribution permissions may be limited.

---

### Built with React, Node.js, MySQL, and an AI multi-agent approach to improve project planning, task coordination, and team productivity.
