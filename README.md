# IDEAHUB Frontend

A colorful, responsive React frontend for the IDEAHUB idea-sharing platform.

## Features

- Dashboard
- Explore/search/filter ideas
- Idea cards and detailed idea pages
- Give-to-Get locked solutions
- Create/publish ideas
- Contribution points
- Rewards and badges
- Leaderboard
- Profile
- Settings
- Likes/comments
- LocalStorage persistence
- Responsive mobile navigation

## Run

```bash
npm install
npm run dev
```

Open http://localhost:5173

## Connecting Spring Boot

The UI currently uses localStorage so it works immediately without a backend.

For the full project, replace the local actions in `src/App.jsx` with calls to your Spring Boot REST API, for example:

GET    /api/ideas
POST   /api/ideas
POST   /api/ideas/{id}/like
GET    /api/ideas/{id}
POST   /api/ideas/{id}/comments
GET    /api/users/me
GET    /api/leaderboard

IMPORTANT:
The Give-to-Get lock must also be enforced by Spring Boot. Never send the protected `solution` field to a user who has not reached the required contribution level.
