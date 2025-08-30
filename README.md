# 🔐 JWTAuthSample

A full-stack implementation of JWT authentication using **.NET 8 Web API** and a **React frontend**.

This project demonstrates:
- User login & registration using JWT
- Secure API endpoints
- React + Axios token management
- Role-ready structure for scaling

---

## 📁 Project Structure

jwt-auth-demo/
├── Backend/ # .NET 8 Web API
│ ├── Controllers/
│ ├── Helpers/
│ ├── Models/
│ ├── Services/
│ └── appsettings.json
│
└── Frontend/ # React app
├── src/
│ ├── App.js
│ ├── AuthContext.js
│ └── api.js

yaml
Copy code

---

## 🚀 Getting Started

### 🔧 Backend – .NET 8 Web API

1. Navigate to the backend directory:

```bash
cd Backend/JwtAuthDemo
Restore dependencies & run:

bash
Copy code
dotnet restore
dotnet run
The API will start on http://localhost:5000.

Key Endpoints
Method	URL	Description
POST	/api/auth/register	Register a user
POST	/api/auth/login	Login and get JWT
GET	/api/secure/protected	Protected route (JWT required)

Default user: test / password

⚛️ Frontend – React App
Navigate to the frontend:

bash
Copy code
cd ../../Frontend
Install dependencies:

bash
Copy code
npm install
Start the app:

bash
Copy code
npm start
React will launch at http://localhost:3000.

🔐 How JWT Works Here
On login, the backend generates a JWT token signed with a secret.
The frontend stores the token in localStorage.
All protected requests automatically include the token via Axios interceptors.
The backend uses JwtBearer middleware to validate the token and authorize access.

🛡 Security Notes
In production, store JWTs in HttpOnly cookies for better security.
Use HTTPS to encrypt traffic.
Extend with refresh tokens for session persistence.
Integrate with real databases and user stores.

🧪 Test It Out
Login using the default user.
Call the protected route using the button in the UI.
Observe that unauthorized users are blocked.

🛠 Built With
.NET 8 Web API
React
JWT Bearer Auth
Axios

