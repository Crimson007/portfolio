# Portfolio Web Application

## Overview
This project is a dynamic portfolio web application designed to showcase skills, projects, and expertise. The application provides a platform for users to interact with the portfolio owner through features like user registration, login, and content management. The backend is powered by Flask, with PostgreSQL as the database.


## Features
- **User Authentication**: Secure user registration and login functionality.
- **Dynamic Content**: Add, update, and delete portfolio items dynamically.
- **Responsive Design**: Fully responsive layout for optimal viewing on all devices.
- **Secure Communication**: Implements secure password hashing and environment-based configurations.

## Technologies Used
- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS, JavaScript
- **Database**: PostgreSQL
- **Environment Management**: Python `dotenv`
- **Version Control**: Git

## Prerequisites
- Python 3.8 or higher
- PostgreSQL 12 or higher
- Virtual environment (e.g., `venv`)
- Git

## Installation Instructions

### Step 1: Clone the Repository
```bash
$ git clone https://github.com/your-repository/portfolio-web.git
$ cd portfolio-web
```

### Step 2: Set Up Virtual Environment
```bash
$ python -m venv venv
$ source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### Step 3: Install Dependencies
```bash
$ pip install -r requirements.txt
```

### Step 4: Set Up PostgreSQL Database
1. Create a new PostgreSQL database:
   ```sql
   CREATE DATABASE portfolio_db;
   ```
2. Create a user and grant privileges:
   ```sql
   CREATE USER mainagideon WITH PASSWORD 'OygM7cdq4GzFvd77';
   GRANT ALL PRIVILEGES ON DATABASE portfolio_db TO mainagideon;
   ```

### Step 5: Configure Environment Variables
Create a `.env` file in the root directory and add the following:
```
SECRET_KEY=your_secret_key
SECURITY_PASSWORD_SALT=your_security_salt
DATABASE_URL=postgresql://mainagideon:OygM7cdq4GzFvd77@localhost/portfolio_db
MAIL_SERVER=smtp.yourmailserver.com
MAIL_PORT=587
MAIL_USE_TLS=True
MAIL_USERNAME=your_email@example.com
MAIL_PASSWORD=your_email_password
UPLOAD_FOLDER=static/uploads
MAX_CONTENT_LENGTH=16777216
```

### Step 6: Initialize the Database
```bash
$ flask db init
$ flask db migrate -m "Initial migration."
$ flask db upgrade
```

### Step 7: Run the Application
```bash
$ flask run
```
Access the application at `http://127.0.0.1:5000/`.

## File Structure
```
portfolio-web/
|├── app/
|   |├── __init__.py
|   |├── models.py
|   |├── routes.py
|   |└── templates/
|├── migrations/
|├── static/
|├── .env
|├── config.py
|├── requirements.txt
|└── app.py
```

## Key Functionalities

### User Authentication
- Implements secure user registration and login using Flask-Security.
- Passwords are hashed using `bcrypt`.

### Dynamic Content Management
- Users can add, update, and delete portfolio items through a user-friendly interface.
- Uploaded files are stored in the `static/uploads` directory.

### Responsive Design
- Ensures compatibility across all devices using modern CSS frameworks.

## Security Measures
- Environment variables are used to secure sensitive information.
- Password hashing ensures user credentials are stored securely.

## Future Enhancements
- Add a REST API for external integrations.
- Implement social media login options.
- Add analytics to track user interactions.

## Troubleshooting

### Common Issues
- **Database Connection Error**: Ensure PostgreSQL is running and the credentials in the `.env` file are correct.
- **Missing Dependencies**: Run `pip install -r requirements.txt` to install all required packages.

### Logs
Check the logs for errors:
```bash
$ flask run --debug
```

## Contribution Guidelines
1. Fork the repository.
2. Create a new branch:
   ```bash
   $ git checkout -b feature-branch-name
   ```
3. Commit your changes:
   ```bash
   $ git commit -m "Add your message here"
   ```
4. Push to the branch:
   ```bash
   $ git push origin feature-branch-name
   ```
5. Open a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For any questions or support, please contact:
- **Name**
#   p o r t f o l i o 
 
 
