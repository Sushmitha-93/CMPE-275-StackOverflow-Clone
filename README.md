# Distributed StackOverflow-Clone
This is a clone of StackOverflow website using MERN stack.

## Table of Contents
- [Tech Stack](#tech-stack)
- [Heavyweight Resource Handling](#heavy-weight-resource-handling)
- [Object Management Policy](#object-management-policy)
- [Frontend](#frontend)
- [Backend](#backend)
- [Getting Started](#getting-started)

## Architecture Diagram
![Architecture Diagram.png](https://github.com/Sushmitha-93/CMPE-275-StackOverflow-Clone/blob/main/Architecture%20Diagram.png)

## Tech Stack
- **Frontend**: React.js
- **Backend**: Node.js, Express.js, Mongoose ORM
- **Database**: MongoDB, AWS S3, Redis
- **Message Queue**: Apache Kafka
- **Performance Testing**: JMeter, Grafana
- **Cloud Services**: AWS EC2, Load Balancer
- **Test Framework**: Mocha

## Heavy Weight Resource Handling
- S3 Bucket stores large data like images for faster access and scalability.
- Connection Pooling reduces database creation time and optimizes resource usage.
- Redis Caching accelerates frequently called database queries.
- Kafka Messaging Queue handles API calls, managing the request/response cycle.
- AWS Load Balancer distributes server load for better performance.

## Object Management Policy
- User, Post, Post_tag, Comment, Bookmark, Badge, Vote & Tag are implemented using SQL due to inter-dependencies and complex joins.
- Messages, PostHistory & ReputationHistory use MongoDB for historical and large data.
- MongoDB's document-centric approach handles large data with higher throughput, making it suitable for scaling.

## Frontend
- Axios is used for handling API requests to the backend.
- Redux manages state, aiding in performance optimizations.
- Rich text editors are implemented for posting questions, answers, and comments.
- React Bootstrap is used for styling.
- Pagination is implemented for user and post components.
- Graphical and visualization components are built using Chart.js in the Admin Dashboard.

## Backend
- Objects like User, Post, Post_tag, Comment, Bookmark, Badge, Vote & Tag are implemented using SQL due to inter-dependency and complex joins.
- MongoDB is used for historical data and large tables like Messages, PostHistory & ReputationHistory. MongoDB's document-centric approach is chosen for high throughput and scalability.
- JWT authentication is implemented for authorized API calls. Private routes are created for admin access only

## Getting Started
1. Clone the repository
2. Install dependencies in backend and frontend directories3. 
4. Create MySQL database called stackoverflow
5. Start Kafka and Redis
6. Update connections in .env files in backend and frontend
7. npm start
