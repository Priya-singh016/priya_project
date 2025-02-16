**Task Management System**



The Task Management System is a web application designed to streamline task assignment and tracking within an organization. It is built using a modern tech stack comprising React.js for the frontend, Node.js with Express.js for the backend, and MongoDB for the database. The system incorporates robust user authentication and role-based access control to ensure data security and privacy.

🌐 Features
User Authentication:

The system provides secure authentication for both Managers and Users.
Authentication is implemented using JSON Web Tokens (JWT) to ensure data integrity and confidentiality.
Role-based Access Control:

Distinct roles (Manager and User) are defined with specific privileges.
Managers have the authority to assign tasks to users, while users can view assigned tasks and update their status.
Task Management:

Managers can create tasks and assign them to individual users or teams.
Users have access to their assigned tasks, allowing them to track progress and mark tasks as completed.
Enhanced Security Measures:

Rate limiters are implemented for authentication API endpoints to prevent brute-force attacks.
IP access control is enforced to restrict access to authorized users and devices.
SSL certificate generation and utilization ensure encrypted communication between the server and client, enhancing overall system security.
🖥️ Tech Stack
Frontend:

React.js for building the user interface.
Utilizes CSS and Bootstrap for styling.
Incorporates React Bootstrap for enhanced UI components.
Backend:

Node.js with Express.js for server-side development.
MongoDB serves as the data storage solution.
🎯 Getting Started
Clone the Repository:

https://github.com/solver44/task-managment-mern.git
Install all frontend and backend dependencies:

npm run install-all
Configure Environment Variables:

Change a .env file and configure the following variables:

 PORT=3000
 dbName = data_base_name
 dbUrl = your_mongodb_connection_string
 SALT_ROUNDS = Number of rounds to use, defaults to 10 if omitted
 JWT_SECRET = your_jwt_secret_key
 JWT_EXPIRE = JWT expires session time
Run the Application:

npm start
Access the Application:

Open your browser and navigate to http://localhost:3000.
Backend API
- POST     /api/signup
- POST     /api/login

- GET      /api/tasks
- GET      /api/tasks/:taskId
- GET      /api/tasks/filter/byUser
- GET      /api/tasks/filter/byStatus
- GET      /api/tasks/data/dashboard
- POST     /api/tasks
- PUT      /api/tasks/:taskId
- PUT      /api/tasks/submit/:taskId
- DELETE   /api/tasks/:taskId

- GET      /api/users
- GET      /api/users/:userId
- POST     /api/users
- PUT      /api/users/:userId
- DELETE   /api/users/:userId
npm scripts
Located at the root directory:

npm start: Initiates both backend and frontend servers concurrently.
npm run dev-server: Initiates only the backend server.
npm run dev-client: Initiates only the frontend development server.
npm run install-all: Installs all dependencies and dev-dependencies required at the root, frontend, and backend.
npm run start-ssl: Initiates client server with SSL certificates.
npm run generate-ssl: Generates SSL certificates (requires installation of mkcert).
Inside frontend folder:

npm start: Starts frontend in development mode
npm run build: Builds the frontend for production to the build folder
Inside backend folder:

npm run dev: Starts backend using nodemon.
npm start: Starts backend without nodemon.
