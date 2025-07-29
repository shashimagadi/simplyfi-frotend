 Project Description  :-
This is a full-stack MERN application with two types of users: Author and User (Reader).

Authors can create articles and receive notifications when their articles are liked.

Users can only view and like articles.

Redis is used to cache likes and views, reducing load on MongoDB.




Start backend:
npm run dev




User Roles :-
1. Author
Can create articles.
Can view a dashboard with their articles.
Receives notifications when someone likes their article.


2. User (Reader) :-
Can view all published articles.
Can like articles.
Cannot create articles or view notifications.


 Application Flow :-
User logs in with name and phone number.
Based on login, a role (author/user) is stored in localStorage.
Role determines what the user can see:
Author → Create Article, Notifications, My Articles.
User → View and Like Articles only.
When a user views or likes an article:
Like/View count is updated in Redis.
Redis reduces repeated access to MongoDB.
When a User likes an article:
A notification is created for the Author.


 Technology Stack:-
Frontend: React, Material UI
Backend: Node.js, Express
Database: MongoDB
Caching: Redis
Others: LocalStorage for session management


Key Features:-
Login with name and phone number.
Role-based access (author/user).
Author can post articles.
User can like/view articles.
Likes and Views cached using Redis.
Real-time notifications for Authors.
Responsive UI.


i have .env file , didnot push it github
