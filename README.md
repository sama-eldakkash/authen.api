#  Auth API – Role-Based Access Control with JWT

A simple Node.js + Express.js authentication API with JWT, rate limiting, role-based authorization, and profile management.

---

##  Setup Instructions

1. Clone the repo or download the project.
2. Run `npm install` to install dependencies.
3. Create a `.env` file with:

```env
PORT=3000
JWT_SECRET=your_jwt_secret_here



##  start the server
node server.js
The server will run on http://localhost:3000.


##  Features Implemented
 User Registration with strong password validation

 Secure Login with  passwords

 JWT Token generation for session security

 Protected Routes (require valid token)

 Role-Based Access Control (user, moderator)

 Profile viewing and updating (email/password)

 Admin route to update user roles

 Rate Limiting for register and login routes


 ##  How to Test Endpoints

 All routes prefixed with /api
Use Postman or similar tools to test the endpoints.
For protected routes, include:
Authorization: Bearer <your_token_here> in the headers 

    Public route
GET /api/public

 Authenticated route
GET /api/protected

 Moderator route
GET /api/moderator (Requires moderator or admin role)

 Profile routes
GET /api/profile

PUT /api/profile

 Update Role (Admin only)
PUT /api/users/:id/role


## Notes
Password must be strong: minimum 8 chars, include number & special char.

JWT tokens expire in 1 hour.

Rate limiter limits repeated login/register attempts.

