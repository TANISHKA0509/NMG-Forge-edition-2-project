# Forge2 Kanban Board – Multi-Agent AI Project Management System

A lightweight Trello-inspired Kanban backend built as part of the **NMG Forge 2 Edition 2 Qualifier**. This project demonstrates how multiple AI agents can collaborate with a human-in-the-loop workflow to design, develop, and deploy a functional project management system.

The application provides REST APIs for managing boards, lists, cards, members, labels, and due dates while showcasing autonomous software development using **Hermes** and **OpenClaw**.

---

# Problem Statement

Modern teams often struggle to efficiently organize tasks, assign responsibilities, and monitor project progress. Existing project management tools are frequently too complex for small teams, student projects, and rapid collaboration.

This project aims to provide a lightweight Kanban-based task management system that enables users to:

* Organize work using boards and lists
* Manage tasks across different stages
* Assign responsibilities to team members
* Track deadlines and progress
* Improve collaboration through a simple interface

Additionally, the project demonstrates **multi-agent software development**, where AI agents collaborate to plan, implement, and maintain the application.

---

# Project Objective

Build a functional Trello-style Kanban backend using:

* Laravel REST APIs
* SQLite Database
* Hermes (Planning Agent)
* OpenClaw (Coding Agent)
* Slack (Human-in-the-loop Communication)

---

# Features

## Board Management

* Create boards
* Retrieve all boards
* Update board details
* Delete boards

## List Management

Each board can contain multiple lists such as:

* To Do
* In Progress
* Done

Users can also create custom workflow stages.

## Card Management

Cards support:

* Title
* Description
* Status updates
* Editing and deletion
* Movement between lists

## Labels & Tags

* Add labels to cards
* Categorize tasks efficiently

## Member Assignment

* Assign tasks to members
* Track responsibilities

## Due Dates

* Set deadlines for tasks
* Highlight overdue tasks

---

# System Architecture

```text
Human User
      ↓
Slack Workspace
      ↓
Hermes Agent (Brain)
      ↓
OpenClaw Agent (Hands)
      ↓
Laravel REST API
      ↓
SQLite Database
```

---

# Multi-Agent Workflow

The development process follows a human-supervised AI workflow:

1. Human defines project requirements.
2. Hermes performs planning and task decomposition.
3. OpenClaw implements features and generates code.
4. Human reviews and approves outputs.
5. Changes are committed and deployed.

---

# Technology Stack

## Backend

* Laravel 12
* PHP 8.2+
* SQLite
* REST APIs

## AI Agent Stack

* Hermes
* OpenClaw
* Slack Integration

## Deployment

* Railway

---

# Database Design

### Entities

* Boards
* Lists
* Cards
* Members
* Tags

### Relationships

```text
Board
 └── Lists
      └── Cards
           ├── Tags
           └── Assigned Members
```

---

# Repository Structure

```text
forge2-kanban/

├── app/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
├── routes/
├── storage/
├── tests/

├── skills/
├── evidence/
├── slack-export/

├── README.md
├── ARCHITECTURE.md
├── agent-log.md
└── .env.example
```

---

# Requirements

* PHP 8.2 or newer
* Composer
* SQLite or any Laravel-supported database

---

# Installation

Clone the repository:

```bash
git clone <repository-url>
cd forge2-kanban
```

Install dependencies:

```bash
composer install
```

Create environment file:

```bash
cp .env.example .env
php artisan key:generate
```

---

# Database Setup

The project uses SQLite by default.

Create the SQLite database:

```bash
touch database/database.sqlite
```

Run migrations:

```bash
php artisan migrate
```

---

# Running the Application

Start the Laravel development server:

```bash
php artisan serve
```

The application will be available at:

```text
http://127.0.0.1:8000
```

---

# API Capabilities

### Boards

* Create Board
* Get All Boards
* Update Board
* Delete Board

### Lists

* Create List
* Retrieve Lists
* Update List
* Delete List

### Cards

* Create Card
* Update Card
* Move Card Between Lists
* Delete Card

### Additional Functionalities

* Labels & Tags
* Member Assignment
* Due Date Tracking
* Overdue Task Detection

---

# Deployment

The backend service is deployed on **Railway**.

### Live API

```text
https://your-project.up.railway.app
```

---

# Evidence

This repository also contains:

* Agent execution logs
* Slack communication screenshots
* Architecture documentation
* Autonomous execution evidence
* Deployment proof
* Walkthrough video/GIF

---

# Forge Qualifier Alignment

This project was specifically designed to satisfy the requirements of the **NMG Forge 2 Edition 2 Qualifier**.

✔ Multi-agent setup

✔ Human-in-the-loop workflow

✔ Slack ↔ Hermes ↔ OpenClaw interaction loop

✔ Autonomous planning and execution

✔ Functional Kanban backend APIs

✔ Documentation and evidence collection

---

# Future Improvements

* Authentication & Authorization
* Notifications
* Real-time updates using WebSockets
* Analytics and reporting dashboard
* Frontend integration

---

# License

This project is licensed under the **MIT License**.
