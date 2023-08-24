# 🚀 Next-Auth with Express, MongoDB, and TailwindCSS

This repository showcases a full-stack authentication solution, combining:
- **Next.js** for frontend development, styled with the aesthetics of **TailwindCSS**. 🎨
- **Express.js** for backend API routes and logic. 🖥️
- **MongoDB** as the go-to database. 🗄️

## 🏛 Architecture

- **Frontend**: Combining Next.js, TailwindCSS, and the `next-auth` package, we offer a seamless user experience and session management.
  
- **Backend**: Express.js provides our API routes handling user registration, login, JWT creation, and validation. 🎩
  
- **Database**: MongoDB ensures secure storage of user details. Passwords are stored securely, hashed with bcrypt. 🔐

## 🔒 How Authentication Works 

1. **User Registration**:
    - Input email and password. 📧
    - Passwords are hashed using bcrypt before storage.
    - Successful registration redirects to the login page. 👣

2. **User Login**:
    - Provide your email and password. 🌐
    - Express.js verifies credentials against MongoDB.
    - On successful authentication, receive a JWT as an HttpOnly cookie. 🍪

3. **Authenticated Requests**:
    - For authenticated requests, the browser sends the JWT cookie automatically. 🌍
    - Express verifies the JWT on each request. 

4. **Session Management on Frontend**:
    - `next-auth` manages user sessions on the frontend. 🌈
    - Use utilities like `useSession` to render content based on authentication state. 📊

5. **Logout**:
    - Logout to end the session. 🔚
    - The JWT cookie is cleared. 🔄

## 💻 Local Setup 

1. **Clone the Repo**:
    ```bash
    git clone https://github.com/adherb/next-auth-express-mongo.git
    ```

2. **Install Dependencies**:
    ```bash
    yarn install
    ```

3. **Environment Variables**:
    - Rename `.env.example` to `.env`. 🔧
    - Update with required environment variables.

4. **Run the Development Server**:
    ```bash
    yarn dev
    ```

5. Visit `http://localhost:3000` in your browser. 🌍
