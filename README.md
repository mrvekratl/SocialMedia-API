# 📱 SocialMedia API

A scalable and modular **Social Media API** built with **ASP.NET Core Web API**, designed to support essential features such as user management, posts, comments, likes, and following mechanisms. The project applies **SOLID principles**, utilizes **Entity Framework Core**, and follows a clean, layered architecture for maintainability and scalability.

---

## 🏗️ Project Structure

The solution is organized into the following projects:

- **SocialMediaApp.API**:  
  Hosts the API controllers, request/response handling, Swagger documentation, middleware, and configuration files.

- **SocialMediaApp.Core**:  
  Contains domain entities, service interfaces, and business rules.

- **SocialMediaApp.Infrastructure**:  
  Implements the service interfaces, data access logic (repositories), authentication, and third-party integrations (e.g., JWT, email, logging).

---

## 📚 Features

### ✅ Authentication & Authorization

- Secure login and registration using **JWT-based authentication**.
- Role-based authorization for protected endpoints.

### 🧑‍🤝‍🧑 User Management

- Register, log in, update profile
- Retrieve user info by ID or username
- Follow / unfollow users
- View followers and followings

### 📝 Post Management

- Create, update, delete, and view posts
- List all posts or posts from followed users
- Search posts by keywords or hashtags

### 💬 Comment System

- Add comments to posts
- Delete user comments

### ❤️ Like System

- Like or unlike a post
- Count and view likes per post

### 🔒 Security

- Passwords are hashed using **ASP.NET Identity PasswordHasher**
- JWT tokens signed with symmetric security key
- Secret scanning enabled with GitHub Push Protection

---

## 🔌 API Endpoints Overview

Here are some of the main endpoints grouped by feature:

### Auth Endpoints

- `POST /api/auth/register` – Register a new user  
- `POST /api/auth/login` – Log in and receive a JWT token  

### User Endpoints

- `GET /api/users/{id}` – Get user by ID  
- `GET /api/users/username/{username}` – Get user by username  
- `PUT /api/users/{id}` – Update user info  
- `GET /api/users/{id}/followers` – List followers  
- `GET /api/users/{id}/followings` – List followings  
- `POST /api/users/{id}/follow` – Follow a user  
- `DELETE /api/users/{id}/unfollow` – Unfollow a user  

### Post Endpoints

- `POST /api/posts` – Create a new post  
- `GET /api/posts` – List all posts  
- `GET /api/posts/{id}` – View a specific post  
- `PUT /api/posts/{id}` – Update post  
- `DELETE /api/posts/{id}` – Delete post  
- `GET /api/posts/search?query={keyword}` – Search posts by keyword  

### Comment Endpoints

- `POST /api/posts/{postId}/comments` – Add comment  
- `DELETE /api/comments/{id}` – Delete comment  

### Like Endpoints

- `POST /api/posts/{postId}/like` – Like post  
- `DELETE /api/posts/{postId}/like` – Unlike post  

---


