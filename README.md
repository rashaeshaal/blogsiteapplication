# Blog Application

## Project Overview
This is a full-stack blog application built using Django for the backend and React for the frontend. It allows users to create, read, update, and delete blog posts. The application features user authentication and a user-friendly interface for both readers and authors.

### Key Features
- User registration and authentication
- Create, read, update, and delete blog posts
- User profile management
- Responsive design for mobile and desktop

## Setup and Installation Steps

### Prerequisites
- **Python 3.8+**
- **Node.js 14+**
- **PostgreSQL** (or MySQL)
- **Docker** (optional)

### Clone the Repository

git clone https://github.com/rashaeshaal/blogsiteapplication.git
cd Blogapp-backend
cd backend
Create a virtual environment and activate it:

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:

pip install -r requirements.txt
Configure your database settings in blogproject/settings.py.

Run the migrations:

python manage.py migrate
Create a superuser to access the admin panel:


Frontend Setup
Navigate to the frontend directory:

cd ../frontend
Install the required packages:

npm install

API Documentation (REST Endpoints)
Authentication
POST /api/register/: Register a new user.

Request Body:
json

{
  "username": "string",
  "email": "string",
  "password": "string"
}
Response: User object with authentication token.
POST /api/login/: Log in an existing user.

Request Body:
json

{
  "username": "string",
  "password": "string"
}
Response: User object with authentication token.
POST /api/logout/: Log out the authenticated user.

Response: Success message.
Blog Posts
GET /api/posts/: Retrieve all blog posts.

Response: List of blog posts.
GET /api/posts/<id>/: Retrieve a specific blog post by ID.

Response: Blog post object.
POST /api/posts/: Create a new blog post.

Request Body:
json

{
  "title": "string",
  "content": "string"
}
Response: Created blog post object.
PUT /api/posts/<id>/: Update a blog post by ID.

Request Body:
json

{
  "title": "string",
  "content": "string"
}
Response: Updated blog post object.
DELETE /api/posts/<id>/: Delete a blog post by ID.

Response: Success message.
User Profile
GET /api/profile/: Retrieve the authenticated user's profile.

Response: User profile object.
PUT /api/profile/: Update the authenticated user's profile.

Request Body:
json

{
  "username": "string",
  "email": "string"
}
Response: Updated user profile object.


