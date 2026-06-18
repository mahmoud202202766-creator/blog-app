# React Blog App

A blog application built with **React** and **Axios**, demonstrating full CRUD (Create, Read, Update, Delete) operations connected to a live REST API. No localStorage is used — all data is persisted remotely via [MockAPI](https://mockapi.io), so posts remain available across sessions and for every visitor.

## Features

- **Create** new blog posts with a title and body
- **Read** all posts on the homepage, with individual post pages
- **Update** existing posts via an edit form
- **Delete** posts
- **Search** posts by title
- Loading and error states while fetching data
- Client-side routing between Home, Post, Edit, and About pages

## Tech Stack

- **React** (Vite)
- **Axios** — HTTP client for API requests
- **easy-peasy** — global state management (store, actions, thunks, computed values)
- **React Router** — client-side routing
- **MockAPI.io** — live REST API used as the backend/data store

## How It Works

Instead of using `localStorage` (which only persists data on a single browser), this app talks to a real REST API. All CRUD operations go through Axios:

```js
// Get all posts
api.get("/posts")

// Create a post
api.post("/posts", newPost)

// Update a post
api.put(`/posts/${id}`, updatedPost)

// Delete a post
api.delete(`/posts/${id}`)
```

The app's global state (posts list, search results, form inputs) is managed with **easy-peasy**, keeping components clean and centralizing async logic in thunks.

## Getting Started

```bash
# Clone the repo
git clone https://github.com/mahmoud202202766-creator/blog-app.git

# Install dependencies
cd blog-app
npm install

# Run the dev server
npm run dev
```

## Live Demo

(https://blog-app-two-dusky.vercel.app/)
## Author

**Mahmoud Elhayad** — Front-End Developer (React.js & JavaScript)
[GitHub](https://github.com/mahmoud202202766-creator)
