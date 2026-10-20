---
name: sync_docs
description: >-
  Synchronize both production_artifacts/Technical_Specification.md and the root
  README.md with version histories, architectural changes, development updates,
  environment prerequisites, and next steps. Use at the end of every development
  or bug-fixing cycle once @qa and @devops verify the build.
---

# Skill: Sync Docs (`sync_docs`)

## Objective
Your goal as the **Product Manager (`@pm`)** and **Technical Writer (`@technicalwriter`)** is to keep both `production_artifacts/Technical_Specification.md` and the root `README.md` continuously synchronized with version histories, as-built architectural updates, bug fixes, runtime prerequisites, and next steps at the conclusion of every development or bug-fixing cycle.

## Rules of Engagement
- **Dual-Target Synchronization**: Both `production_artifacts/Technical_Specification.md` and the root `README.md` MUST be updated in tandem after `@qa` and `@devops` verify the build.
- **Historical Preservation**: Never overwrite or delete prior version history entries in either document. Always append the new version entry with a timestamp and semantic version increment (e.g., `v0.1` -> `v0.2` for features, `v0.1.1` for bug-fix cycles).
- **As-Built Accuracy**: Any implementation adjustments, dependency additions, or bug fixes introduced in `app_build/` during engineering, QA auditing, or DevOps deployment must be reflected accurately in both documents.

---

## Execution Instructions

### Phase 1: Product Manager (`@pm`) — Update `production_artifacts/Technical_Specification.md`
1. **Audit As-Built Implementation**: Compare the current `production_artifacts/Technical_Specification.md` against the verified code and configurations inside `app_build/`.
2. **Synchronize Technical Architecture**:
   - Update the **Executive Summary**, **Requirements**, **Architecture & Tech Stack**, **API / Data Models**, and **State Management** sections to reflect any new features, refactors, or bug-fix resolutions implemented during the cycle.
3. **Log Specification Version History**:
   - Maintain a dedicated **Revision & Version History** section in `production_artifacts/Technical_Specification.md`.
   - Append a new version entry including:
     - **Version & Date**: Semantic version number and current ISO date (`YYYY-MM-DD`).
     - **Authoring Agents**: `@pm` (verified with `@qa` and `@devops`).
     - **Architectural & Development Changes**: Summary of spec updates, resolved defects, or dependency adjustments.
     - **Upcoming Roadmap / Next Steps**: Planned architectural evolution for the next iteration.

### Phase 2: Technical Writer (`@technicalwriter`) — Update Root `README.md`
1. **Analyze Spec & Build Assets**: Review the newly updated `production_artifacts/Technical_Specification.md` and inspect configuration files in `app_build/` (e.g., `package.json`, `requirements.txt`, `pyproject.toml`, `.env.example`, `Dockerfile`).
2. **Append Milestone to Version History & Status**:
   - Under `## 📅 Version History & Status` in the root `README.md`, append the new milestone entry with:
     - **Timestamp & Version**: Current date (`YYYY-MM-DD`) and version tag matching the specification.
     - **Completed Objectives & Developments**: High-level summary of newly built features, architectural refinements, and bug fixes verified by `@qa` and `@devops`.
     - **Next Steps**: What the upcoming development phase entails based on the specification roadmap.
3. **Synchronize Prerequisites & Local Development Setup**:
   - Ensure the root `README.md` contains an up-to-date, cross-platform **Prerequisites & Local Development Setup** section detailing:
     - **Minimum Runtime Versions**: Required runtimes (e.g., Node.js LTS, Python, Go, Docker) and version managers (`nvm`, `fnm`, `uv`).
     - **Required Environment Variables**: Structured table documenting variables from `.env.example` and `.env` setup.
     - **Local Execution Commands**: Step-by-step commands to install, build, test, and run the application locally.
     - **Mock Credentials & Bypasses**: Any test accounts, seed data, or offline bypasses for rapid developer onboarding.
4. **Commit Documentation**: Save all updates cleanly in GitHub-flavored Markdown to both `production_artifacts/Technical_Specification.md` and the root `README.md`.
