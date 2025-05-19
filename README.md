
# Kanban Board with JWT Authentication

## Description

This project is a **Kanban Board** application designed to help manage and track tasks within a team. It includes user authentication using **JSON Web Tokens (JWT)** for secure access. The backend is built with **Node.js**, **Express.js**, and **PostgreSQL**, while the frontend is developed with **React** and **Vite**.

This application allows users to:
- Log in with secure authentication.
- View and manage tasks organized by different stages (To Do, In Progress, Done).
- Use a PostgreSQL database to store task and user data.

## Features
- **JWT Authentication**: Secure login system using JWT for user authentication.
- **Kanban Board**: Organize tasks into different columns: **To Do**, **In Progress**, and **Done**.
- **Task Management**: Add, update, and delete tasks.
- **Responsive UI**: Designed to work seamlessly on both desktop and mobile.
- **PostgreSQL Database**: Tasks and user data are stored in a PostgreSQL database hosted on Render.

## Tech Stack
- **Frontend**: React, Vite, CSS 
- **Backend**: Node.js, Express.js
- **Database**: PostgreSQL (hosted on Render)
- **Authentication**: JWT (JSON Web Token)
- **API Requests**: Fetch API (Axios or similar library)

## Installation and Setup

### Prerequisites
Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/en/) (LTS version recommended)
- [PostgreSQL](https://www.postgresql.org/) (locally or use Render for remote hosting)
- [Git](https://git-scm.com/)

### Clone the Repository

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your_username/kanban-board.git
   cd kanban-board
   ```

### Backend Setup

1. Navigate to the backend folder:
   ```bash
   cd server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory and add your database and JWT credentials:
   ```env
   DB_HOST=your-database-host
   DB_PORT=5432
   DB_NAME=kanban_db
   DB_USER=your-database-user
   DB_PASSWORD=your-database-password
   JWT_SECRET_KEY=your-secure-jwt-secret
   ```

4. Run the backend:
   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to the frontend folder:
   ```bash
   cd client
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open the app in your browser:
   ```
   http://localhost:5173
   ```

### Database Setup (PostgreSQL)

1. **Locally**:
   If you're running the database locally, ensure PostgreSQL is installed and running. You can use `pgAdmin` or **DBeaver** to create a new database (e.g., `kanban_db`) and a user (e.g., `user123`).

2. **On Render**:
   If you're using **Render** for hosting PostgreSQL, create a database through the Render dashboard and copy the **connection details** into your `.env` file for the backend.

### Seeding the Database (Optional)

To populate the database with initial data, you can run the seed script:
```bash
npm run seed
```

This will insert sample tasks and user data into the database.

## Usage

- **Login**: Users can log in using the `/auth/login` endpoint, which returns a JWT for authentication.
- **Tasks**: Tasks can be created, updated, and deleted. They are displayed in columns based on their current status (e.g., "To Do", "In Progress", "Done").
- **JWT Authentication**: The token is stored in `localStorage` for client-side access, and the `Authorization` header is added to every API request that requires authentication.

## Deployment

### Deploying Backend to Render

1. Push your code to a **GitHub repository**.
2. Go to [Render](https://render.com/) and create a **new Web Service**.
3. Link your **GitHub repository**.
4. Set environment variables in Render:
   - `DB_HOST`, `DB_PORT`, `DB_USER`, `DB_PASSWORD`, `DB_NAME`, and `JWT_SECRET_KEY`.
5. Deploy the backend.

### Deploying Frontend to Render (Optional)

1. Push your frontend code to **GitHub** (if not already done).
2. Go to **Render**, create a **new Static Site**, and link your **GitHub repo**.
3. Configure the **build settings** to use `npm run build`.
4. Deploy the frontend.

### Production Configuration

Make sure to set **production environment variables** in both the frontend and backend on Render for security and optimal performance.

## API Routes

- **POST** `/auth/login`: Logs in a user and returns a JWT.
- **GET** `/tasks`: Fetches all tasks.
- **POST** `/tasks`: Creates a new task.
- **PUT** `/tasks/:id`: Updates a task.
- **DELETE** `/tasks/:id`: Deletes a task.

## Contributing

Feel free to fork this repository, make changes, and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License.

