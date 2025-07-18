# Flask Notes Website

A simple note-taking web application built with Flask that allows users to create accounts, log in, and manage their personal notes.

## Features

- **User Authentication**: Sign up, login, and logout functionality
- **Personal Notes**: Create, view, and delete personal notes
- **Secure Storage**: User passwords are securely hashed
- **Responsive Design**: Bootstrap-powered responsive UI
- **Database Integration**: SQLite database with SQLAlchemy ORM

## Technologies Used

- **Backend**: Flask (Python web framework)
- **Database**: SQLite with Flask-SQLAlchemy ORM
- **Authentication**: Flask-Login for session management
- **Password Security**: Werkzeug for password hashing
- **Frontend**: HTML, CSS, Bootstrap 4
- **JavaScript**: Vanilla JS for delete functionality

## Project Structure

```
Website---Flask/
├── main.py                 # Application entry point
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
└── website/
    ├── __init__.py        # Flask app factory
    ├── auth.py            # Authentication routes
    ├── views.py           # Main application routes
    ├── models.py          # Database models
    ├── static/            # Static files (CSS, JS, images)
    └── templates/         # HTML templates
        ├── base.html      # Base template
        ├── home.html      # Notes dashboard
        ├── login.html     # Login page
        ├── logout.html    # Logout page
        └── signup.html    # Sign up page
```

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/muralidharan-1708/Website---Flask.git
   cd Website---Flask
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv .venv
   ```

3. **Activate the virtual environment**:
   - **Windows**:
     ```bash
     .venv\Scripts\activate
     ```
   - **macOS/Linux**:
     ```bash
     source .venv/bin/activate
     ```

4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Run the application**:
   ```bash
   python main.py
   ```

2. **Open your browser** and navigate to `http://127.0.0.1:5000`

3. **Create an account** by clicking "Sign Up"

4. **Log in** with your credentials

5. **Start creating notes** on the home page

## Features Overview

### User Management
- **Sign Up**: Create new user accounts with email validation
- **Login**: Secure user authentication
- **Logout**: End user sessions safely

### Note Management
- **Create Notes**: Add new notes from the home page
- **View Notes**: All user notes displayed on the dashboard
- **Delete Notes**: Remove notes with a single click

## Database Models

### User Model
- `id`: Primary key
- `email`: Unique user email
- `password`: Hashed password
- `name`: User's display name
- `notes`: Relationship to user's notes

### Note Model
- `id`: Primary key
- `data`: Note content
- `date`: Creation timestamp
- `user_id`: Foreign key to user

## Security Features

- Password hashing using Werkzeug
- User session management with Flask-Login
- CSRF protection with secret keys
- User authorization for note operations

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

**Muralidharan** - [muralidharan-1708](https://github.com/muralidharan-1708)