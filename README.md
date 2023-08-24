Next-Auth with Express and MongoDB 🚀

This repository provides a full-stack authentication solution combining the best of three worlds: Next.js for the frontend, Express.js for the backend, and MongoDB as the database.

Architecture 🏛
Frontend: Uses Next.js and the next-auth package to manage user sessions and authentication UI/UX. 🎨

Backend: Uses Express.js to provide API routes for user registration, login, and other related endpoints. It also manages JWT creation and validation. 🖥️

Database: MongoDB is used to store user details, including encrypted passwords. 🗄️

How Authentication Works 🔒
User Registration:

Users provide their email and password to register. 📧
Passwords are securely hashed using bcrypt before being stored in MongoDB. 🔐
Upon successful registration, users are directed to the login page. 👣
User Login:

Users provide their email and password to login. 🌐
The Express server verifies the credentials against the MongoDB database. ✅
Upon successful authentication, the server generates a JWT (JSON Web Token) and sends it as an HttpOnly cookie to the client. 🍪
Authenticated Requests:

For subsequent requests that require authentication, the browser automatically sends the JWT in the cookie. 🌍
The Express server verifies the JWT on each request. If valid, the request is processed; if not, an error is returned. ❌
Session Management on Frontend:

next-auth is utilized on the frontend to manage user sessions. 🌈
When a user logs in, next-auth maintains a session on the client-side, offering utilities and hooks (e.g., useSession) to conditionally render content based on the user's authentication state. 📊
Logout:

Users can log out, invalidating their session. 🔚
The JWT cookie is cleared, ensuring the user has to log in again to make authenticated requests. 🔄
Local Setup 💻
Clone the Repo:

bash
Copy code
git clone https://github.com/yourusername/next-auth-express-mongo.git
Install Dependencies:

bash
Copy code
npm install
Environment Variables:

Rename .env.example to .env. 🔧
Fill in the necessary environment variables, such as MongoDB connection string, JWT secret, etc.
Running the Development Server:

bash
Copy code
npm run dev
Navigate to http://localhost:3000 in your browser. 🌍

Contributing 🤝
Please create a new GitHub issue for any bugs, enhancements, or feature requests. Pull requests are welcome – ensure your changes are on a separate branch.
