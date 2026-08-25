# 🤖 SDD Team Template (v0.1)

Welcome to the **Specification-Driven Development (SDD) Team Template**. This repository provides an autonomous multi-agent development workflow designed to turn raw software ideas into fully engineered, audited, and deployed applications.

---

## 📅 Version History & Status

### v0.1 — Initial Template Release (2026-08-25)
* **Milestone**: Established template structure, multi-agent roles, pipeline skills, and baseline documentation.
* **Status**: Ready to be cloned/copied for new project setup.

---

## 🏛 Architecture & Folder Structure

```
.
├── .agents/
│   ├── agents.md               # Autonomous Agent Role Definitions (@pm, @engineer, @qa, @devops, @technicalwriter)
│   ├── skills/
│   │   ├── startcycle.md       # Pipeline Orchestration Skill (/startcycle <idea>)
│   │   ├── write_specs.md      # PM Skill: Specs & Approval Gate
│   │   ├── generate_code.md    # Engineer Skill: Code Generation
│   │   ├── audit_code.md       # QA Skill: Code Auditing & Bug Fixing
│   │   ├── deply_app.md        # DevOps Skill: Local Server Launch
│   │   └── update_readme.md    # Technical Writer Skill: Documentation Updates
│   └── workflows/              # Custom automated workflow configurations
├── app_build/                  # Target directory for generated application source code
└── production_artifacts/       # Target directory for Technical Specifications & Architecture docs
```

---

## 🚀 How to Copy File Structure to a New Project

To create a new project using this template:

### Option A: Using PowerShell (Windows)
```powershell
# 1. Create your new project folder
New-Item -ItemType Directory -Path "C:\Projects\MyNewProject"

# 2. Copy the template structure into the new folder
Copy-Item -Path "c:\Projects\SDD Team Template\.agents" -Destination "C:\Projects\MyNewProject\.agents" -Recurse
New-Item -ItemType Directory -Path "C:\Projects\MyNewProject\app_build"
New-Item -ItemType Directory -Path "C:\Projects\MyNewProject\production_artifacts"
Copy-Item -Path "c:\Projects\SDD Team Template\README.md" -Destination "C:\Projects\MyNewProject\README.md"
```

### Option B: Using Command Prompt (cmd)
```cmd
mkdir "C:\Projects\MyNewProject"
xcopy "c:\Projects\SDD Team Template\.agents" "C:\Projects\MyNewProject\.agents" /E /I /H
mkdir "C:\Projects\MyNewProject\app_build"
mkdir "C:\Projects\MyNewProject\production_artifacts"
copy "c:\Projects\SDD Team Template\README.md" "C:\Projects\MyNewProject\README.md"
```

> [!TIP]
> Ensure the `.agents/` folder is present in your workspace root so the AI agent team can automatically recognize their roles and skills.

---

## 🔄 How to Initiate the Development Startcycle

To launch the autonomous development pipeline on a new idea, type the following command in the chat interface:

```bash
/startcycle <your project idea or user story>
```

### Development Pipeline Workflow:

1. **Step 1: Product Manager (`@pm`) — `write_specs.md`**
   - Analyzes your idea and drafts `production_artifacts/Technical_Specification.md`.
   - Outlines tech stack, API architecture, data models, and requirements.
   - **Approval Gate**: Pauses execution and asks for your approval. You can approve or add comments directly inside `Technical_Specification.md` to request revisions.

2. **Step 2: Full-Stack Engineer (`@engineer`) — `generate_code.md`**
   - Takes the approved spec and generates production-ready source code in `app_build/`.

3. **Step 3: QA Engineer (`@qa`) — `audit_code.md`**
   - Audits `app_build/` for syntax errors, missing dependencies (`package.json`, `requirements.txt`), security risks, and unhandled edge cases.
   - Automatically fixes and commits revisions.

4. **Step 4: DevOps Master (`@devops`) — `deply_app.md`**
   - Detects the project stack, installs required packages, and launches a local background server.
   - Provides a clickable `localhost` URL to view the live application.

5. **Step 5: Technical Writer (`@technicalwriter`) — `update_readme.md`**
   - Documents completed objectives, updates `README.md` with the new version milestone, and summarizes next steps.

---

## 📝 Documentation Standards & Writing Guidelines

Documentation in this repository is maintained automatically and updated systematically after every development cycle:

- **Technical Specifications**: Saved to `production_artifacts/Technical_Specification.md`. Must include Executive Summary, System Architecture, Tech Stack, and Data Flow.
- **Project Progress & History**: Recorded in the root `README.md`. Historical milestone entries are preserved chronologically; new cycle completion summaries are appended under **Version History & Status**.
- **Code Documentation**: Code inside `app_build/` must include inline JSDoc/Docstrings and explicit `README.md` files where applicable for framework specific instructions.
