# SignUp-Login-Logout-API-Project

This project provides a user authentication API using Django Rest Framework.

Installation

1. Clone the repository: git clone https://github.com/<username>/<project-name>.git
2. Install the required packages: pip install -r requirements.txt
3. Run database migrations: python manage.py migrate
4. Start the development server: python manage.py runserver

API Endpoints
  
User Signup
Endpoint: POST /api/signup/
  
Request Body:

json
{
    "username": "<username>",
    "password": "<password>",
    "email": "<email>"
}

Response:

json
{
    "user": {
        "id": <user_id>,
        "username": "<username>",
        "email": "<email>"
    },
    "token": "<token>"
}

  
User Login
Endpoint: POST /api/login/

Request Body:

json
{
    "username": "<username>",
    "password": "<password>"
}

Response:

json
{
    "user": {
        "id": <user_id>,
        "username": "<username>",
        "email": "<email>"
    },
    "token": "<token>"
}

  
  
User Logout
Endpoint: POST /api/logout/

Request Headers:

Authorization: Token <token>
Response:

json
{
    "success": true
}

  
Change Password
Endpoint: POST /api/change-password/

Request Headers:

Authorization: Token <token>
Request Body:

json
{
    "old_password": "<old_password>",
    "new_password": "<new_password>"
}

  
Response:

json
{
    "success": true
}
