# Mini Chat App

## Table of Contents

- [Mini Chat App](#mini-chat-app)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Goal](#goal)
  - [Version](#version)
    - [Version 0 (v0.1 on main branch): Mock UI and Fake data](#version-0-v01-on-main-branch-mock-ui-and-fake-data)
  - [UI Screenshots](#ui-screenshots)
  - [Architecture](#architecture)
    - [Database](#database)
    - [Backend](#backend)
    - [Frontend](#frontend)
  - [Technology \& Knowledge](#technology--knowledge)
  - [API testing with Postman](#api-testing-with-postman)
    - [Import Postman Collection](#import-postman-collection)
  - [How to run](#how-to-run)
  - [Fix Bugs](#fix-bugs)
  - [Time Tracking](#time-tracking)
  - [Future Work](#future-work)

## Features

- Fullstack mobile application (Android & iOS), using PostgreSQL, Laravel, FLutter.
- The purpose of this web app is to help users having instant 1-1 chats, connecting with others, ensuring security and speed.
- Main functions:
  - Sign up / Login / Forget password / Change password
  - Add / delete friend (with search)
  - Chat (with text, images, videos), can send / remove message
  - List friends (with search)
- Keyword:

## Goal

- Apply semantic versioning in project, know how to merge, resolve conflicts, interact between branches
- Learn about Flutter, Laravel, PostgreSQL, other concepts.
- Create a mobile application and push it production, on AppStore/CH Play

## Version

### Version 0 (v0.1 on main branch): Mock UI and Fake data

- Target:
  - Know UI flow
  - Mock data JSON
  - Learn Docker, OOP, SOLID, Clean Architecture
  - Choose language: Tiếng Việt, English
  - Create 10 pages with fake data: Login page, Sign up page, Forget pass page, Home page, Chat page, Messaging page, Friend page, Settings page, Change password page, Change language page
  - Git branch: main, hotfix, release, develop, feature
- 7 feature branches for this v0.1:
  - feature/v0.1/fe-project-setup
  - feature/v0.1/fe-auth (Login page, Sign up page, Forget pass page)
  - feature/v0.1/fe-home (Home page - BottomNavigationBar)
  - feature/v0.1/fe-chat-ui (Chat page, messaging page)
  - feature/v0.1/fe-friend-ui (Friend page)
  - feature/v0.1/fe-settings (Settings page, Change password page, Logout)
  - feature/v0.1/fe-multi-language-support (switch between Vietnamese / English language in settings -> Change language page in settings)

## UI Screenshots

## Architecture

### Database

- PostgreSQL: mini_chat_app_db

### Backend

- Laravel (IDE VS Code): mini-chat-app-backend

### Frontend

- Flutter (IDE VS Code): mini-chat-app-frontend
- Structure:
  - assets/: contains images, screenshots, mock data
  - lib/: contains source code with clean architecture + provider
    - core/: contains global configurations and shared resources used across the entire application.
      - constants/: application-wide constants (API endpoints, keys, etc.)
      - localization/: language support
      - network/: network configuration (Dio client, interceptors, API base setup)
      - routes/: Centralized route management for navigation
      - theme/: App-wide UI theme (colors, typography, dark/light mode)
      - utils/: Common helper functions (formatter, etc.)
      - validators/: Form validation logic (email, password, etc.)
    - features/: each feature is isolated and follow the same internal structure: data, domain, presentation
      - features/auth/: handle authentication-related functionally (login, register, forget password, change password, logout)
      - features/chat/: handle realtime messaging features (list conversations, list messages in conversation, search, send / remove message)
      - features/friend/: handle friend system (add / delete friend, search users, friend requests)
      - features/settings/: handle user settings (change language)
      - features/\*/data/: responsible for data operations (API calls, mock data, models, repository impl)
      - features/\*/domain: business logic layer, include entities, repository contracts, and use cases
      - features/\*/presentation: UI layer, pages, state management (provider), and UI widgets
  - pubspec.yaml: configuration file (dependencies, assets, fonts...)
  - Compare folders in features with 4 layer in Clean architecture:
    - Entities: domain/entity, data/model
    - Use case: domain/usecase
    - Interface adapter: domain/repository, data/repository, presentation/provider
    - Frameworks & drivers: data/datasource, core/network, presentation/pages, presentation/widgets

## Technology & Knowledge

- Database:
  - Create database, create table
  - Constraint, Primary key, Foreign key, Unique, Check
  - Index
  - DDL, SQL Constraint, DML, DQL, 3NF
  - ACID
  - Transactions

- Frontend (Flutter):
  - Naming for project: snake_case
  - Naming for folders / files: snake_case
  - Naming for class: PascalCase
  - Naming for variables, functions, attributes, constants, finals: camelCase
  - Naming for enum name: PascalCase
  - Naming for enum value: camelCase
  - Interface = abstract class: abstract class IClassName (for interface) / ClassName.
  - Use relative imports
  - Use definite data types, limit the use of variables.
  - Use If instead of conditional expressions
  - Use cascades operator
  - Use raw string (contains / or $) with r before string: r'...'
  - Don't need initialize variables with null (Flutter automatically do it)
  - Use arrow function
  - Use ListView.Builder for a long list
  - Use const in widgets

- Backend:

- Naming Convention:
  - project name: kebab-case
  - URL request parameter convention: kebab-case
  - git feature naming:
    - kebab-case
    - when code with FE and BE, should have "context prefix", for example: feature/fe-login-ui (Frontend), feature/be-login-api (Backend).

- Commit conventions: -https://viblo.asia/p/dat-ten-commit-message-sao-cho-tinh-nghia-anh-em-chac-chan-ben-lau-OeVKBM605kW

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## API testing with Postman

### Import Postman Collection

- Import this JSON file into your Postman:

## How to run

-

## Fix Bugs

## Time Tracking

| Date | Task | Notes |
| ---------- | -------------------------------------------------------- | . |
| 2026-06-09 | Setup project, create README, initialize Flutter project | . |
| 2026-06-10 | Learn Docker, OOP, Solid, Clean Architecture | . |
| 2026-06-11 -> 2026-06-12 | Learning MVVM, restructure FE architecture | v0.1 |

## Future Work

- [ ] Update app structure, optimize and clean code.
- [ ] UI : Design the UI better, cleaner.
