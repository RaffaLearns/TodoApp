# Todo App (Express.js)

This is a simple app that allows users to create and manage projects and todos.

## Goals

- Follow git best practices and conventions for naming branches and commits (husky, commitlint).
- Have a clean architecture (MVC) and a maintanable code (TypeScript).
- Return meaningful error messages.
- Implement authentication (passport-jwt)
- Test the code (mocha, chai)
- Have a working version by April 29th (in 10 days)

## API Endpoints

1. `/api/v1/users` (POST)
1. `/api/v1/users/:id` (GET, PATCH, DELETE)
1. `/api/v1/users/:id/profile` (GET, POST, PATCH)
1. `/api/v1/users/:id/todos` (GET, POST)
1. `/api/v1/users/:id/todos/:todoId` (GET, PATCH, DELETE)
1. `/api/v1/users/:id/projects` (GET, POST)
1. `/api/v1/projects/:projectId` (GET, PATCH, DELETE)
1. `/api/v1/projects/:id/todos` (GET, POST)
1. `/api/v1/projects/:id/todos/:todoId` (GET, PATCH, DELETE)

## DB Schema

### Users

- id
- email
- hash
- salt
- createdAt
- profile

### Profiles

- userId
- name
- profilePicture?
- personalTodos[]
- projects[]

### Todos

- id
- createdAt
- dueDate
- title
- body
- doneTimestamp?
- user
- project?

### Projects

- id
- owner
- users[]
- createdAt
- archivedAt?
