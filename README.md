# StudyNotion

An ed‑tech platform built with the MERN stack (ReactJS, NodeJS, MongoDB, ExpressJS).


## Project Description

StudyNotion is a fully functional ed‑tech platform that enables users to create, consume, and rate educational content. The platform aims to provide:

* A seamless and interactive learning experience for students, making education more accessible and engaging.
* A platform for instructors to showcase their expertise and connect with learners across the globe.

In the following sections, we cover the technical details of the platform:

1. System Architecture
2. Front‑end
3. Back‑end
4. Database
5. API Design
6. Deployment
7. Testing
8. Future Enhancements
9. Conclusion

---

## System Architecture

The StudyNotion ed‑tech platform consists of three main components:

1. **Front‑end** (Client)
2. **Back‑end** (Server)
3. **Database**

This client‑server architecture allows the ReactJS front‑end to communicate with the NodeJS/ExpressJS back‑end via RESTful API calls.

### Architecture Diagram

![Architecture Diagram](./architecture-diagram.png)

---

## Front‑end

### Overview

* **Library**: ReactJS
* **State Management**: Redux
* **Styling**: CSS & Tailwind
* **Design Tool**: Figma (prototype available at dummy link)
* **Editor**: VSCode

### Student Pages

* **Homepage**: Introduction & links to course list and profile
* **Course List**: Browse all courses with descriptions and ratings
* **Wishlist**: Saved courses
* **Cart & Checkout**: Purchase flow integration
* **Course Content**: View video and materials
* **User Profile**: View & edit account details

### Instructor Pages

* **Dashboard**: Overview of courses, ratings, feedback
* **Insights**: Course analytics (views, clicks, etc.)
* **Course Management**: Create, update, delete courses
* **Profile**: View & edit instructor details

### Admin (Future Scope)

* **Dashboard**: Platform‑wide metrics
* **Insights**: User/course/revenue analytics
* **Instructor Management**: Manage instructors and courses
* **User Management**

---

## Back‑end

### Architecture & Tech

* **Runtime**: NodeJS
* **Framework**: ExpressJS
* **Database**: MongoDB (via Mongoose ODM)
* **Authentication**: JWT, OTP verification, forgot‑password
* **Password Security**: Bcrypt hashing
* **Media Storage**: Cloudinary

### Features

* **User Auth & Authorization** (students & instructors)
* **Course Management** (CRUD) by instructors
* **Course Consumption** & ratings by students
* **Payment Integration** via Razorpay
* **Markdown Formatting** for course documents

### Data Models

* **Student**: name, email, password, enrolled courses
* **Instructor**: name, email, password, created courses
* **Course**: title, description, instructor ID, media URLs, ratings

---

## Database

* **Primary**: MongoDB Atlas (NoSQL, cloud‑hosted)
* **Media**: Cloudinary (images, videos, documents)

---

## API Design

RESTful endpoints implemented with NodeJS & ExpressJS, exchanging JSON.

| Endpoint                    | Method | Description                          |
| --------------------------- | ------ | ------------------------------------ |
| `/api/auth/signup`          | POST   | Create new user (student/instructor) |
| `/api/auth/login`           | POST   | Authenticate & issue JWT             |
| `/api/auth/verify-otp`      | POST   | Verify email OTP                     |
| `/api/auth/forgot-password` | POST   | Send password reset link             |
| `/api/courses`              | GET    | List all courses                     |
| `/api/courses/:id`          | GET    | Get course details                   |
| `/api/courses`              | POST   | Create a new course                  |
| `/api/courses/:id`          | PUT    | Update existing course               |
| `/api/courses/:id`          | DELETE | Delete a course                      |
| `/api/courses/:id/rate`     | POST   | Rate a course (1–5 stars)            |

**Sample Request/Response**:

```http
GET /api/courses
Host: example.com
Accept: application/json
```

```json
[
  { "_id": "123", "title": "React Basics", "rating": 4.5 },
  { "_id": "456", "title": "NodeJS API Development", "rating": 4.8 }
]
```

---

## Deployment

* **Front‑end**: Vercel (React static hosting)
* **Back‑end**: Render.com or Railway.app (NodeJS & MongoDB)
* **Database**: MongoDB Atlas
* **Media**: Cloudinary

This setup ensures scalability, security, and high availability.

---

## Testing

* **Unit Tests**: Jest & React Testing Library
* **API Tests**: Supertest & Mocha
* **E2E Tests**: Cypress

---

## Future Enhancements

1. **Personalized Learning Paths** (High Priority)
2. **Mobile App** (High Priority)
3. **Machine Learning Recommendations** (Medium)
4. **Gamification (Badges & Leaderboards)** (Medium)
5. **Social Learning (Discussions & Collaboration)** (Medium)
6. **VR/AR Integration** (Low)

These features will improve engagement, personalization, and reach.

---

## Conclusion

StudyNotion is a versatile, intuitive ed‑tech platform designed to provide an immersive learning experience. Built on a robust MERN stack and deployed on modern cloud services, it’s ready for future growth and enhancements.
