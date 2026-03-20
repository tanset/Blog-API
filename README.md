# Blog-API

This is a simple blog application built with **Node.js**, **Express**, and **EJS**. The project demonstrates a basic CRUD (Create, Read, Update, Delete) flow using a separate API server and a client-facing web server.


## How It Works

The system consists of two main components:

### 1. API Server (Data Management)
*   **Port:** Runs on `http://localhost:4000`.
*   **Storage:** Uses an in-memory array (`posts`) to store blog data.
*   **Function:** Handles all data operations. It provides endpoints to get all posts, find a specific post by ID, create new entries, update existing ones using `PATCH`, and delete posts.

### 2. Client Server (User Interface)
*   **Port:** Runs on `http://localhost:3000`.
*   **Function:** This server acts as the interface for users. It uses **Axios** to communicate with the API server and **EJS** to render HTML pages.
*   **Flow:** When a user visits the site, the client server fetches data from the API server and displays it using the `index.ejs` and `modify.ejs` templates.

---

## How to Use

Follow these steps to run the project locally:

### 1. Prerequisites
Ensure you have **Node.js** installed. You will also need to install the following dependencies:
```bash
npm install express body-parser axios ejs
```

### 2. Run the API Server
Open a terminal and run the backend script:
```bash
node index.js
```
*(Note: Replace `index.js` with the filename containing the API code).*
The API will be active at `http://localhost:4000`.

### 3. Run the Client Server
Open a **second** terminal and run the frontend script:
```bash
node server.js
```
*(Note: Replace `server.js` with the filename containing the client code).*
The application will be accessible at `http://localhost:3000`.

### 4. Features
*   **View Posts:** Browse all blog entries on the home page.
*   **Add Post:** Click "New Post" to add a new story.
*   **Edit Post:** Click "Edit" to modify the title, content, or author.
*   **Delete Post:** Click "Delete" to remove a post from the list.

---

## Technical Stack
*   **Backend:** Node.js, Express.js
*   **Frontend:** EJS (Embedded JavaScript templates), CSS
*   **HTTP Client:** Axios
*   **Middleware:** Body-parser
