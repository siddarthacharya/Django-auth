# Django AuthSystem - Role-Based Authentication & Medical Blog

A complete Django authentication system with **Patient** and **Doctor** user roles, extended with a medical blog platform where doctors can create categorized blog posts (with draft feature) and patients can browse published posts.

Built with Django 5.2.4, MySQL, and a JavaScript frontend of your choice.

## 🚀 Features

### User Management
- **Two User Roles**: Patient and Doctor
- **Complete Registration**: First name, last name, username, email, password, address, and profile picture
- **Flexible Login**: Support for both username and email authentication
- **Role-Based Dashboards**: Separate interfaces for patients and doctors
- **Profile Pictures**: Image upload with proper handling
- **Medical Blog System**:  
  - Doctors create posts with title, image, category, summary, content  
  - Draft or publish blog posts  
  - Patients view published posts by category with truncated summaries (15 words)  

### Authentication Features
- ✅ User registration with validation
- ✅ Login/logout functionality
- ✅ Password confirmation validation
- ✅ Unique username and email validation
- ✅ Protected routes with `@login_required`
- ✅ Role-based redirection after login

### Technical Features
- ✅ Custom User model extending AbstractUser
- ✅ MYSQL server
- ✅ Media file handling for uploads
- ✅ Responsive design with raw HTML/CSS
- ✅ Form validation and error handling

## Requirements

- Python 3.8+  
- Django 5.2.4  
- MySQL Server  
- Pillow (for image handling)  
- JavaScript framework/library 
## 🛠️ Local Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/django-authsystem.git
cd django-authsystem/AuthSystem
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run Migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Superuser (Optional)
```bash
python manage.py createsuperuser
```

### 6. Run Development Server
```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000` to access the application.

## 📁 Project Structure

```
AuthSystem/
├── AuthSystem/              # Django project settings and configuration
│   ├── __init__.py
│   ├── asgi.py              # ASGI application entry point
│   ├── settings.py          # Project settings file
│   ├── urls.py              # Root URL configurations
│   └── wsgi.py              # WSGI application entry point
├── README.md                # Project documentation
├── accounts/                # User authentication and profile management
│   ├── __init__.py
│   ├── admin.py             # Admin site configs for accounts
│   ├── apps.py              # App config
│   ├── forms.py             # Forms for signup/login etc.
│   ├── migrations/          # Database migrations
│   ├── models.py            # Custom User models
│   ├── static/              # Static files (CSS, JS, images)
│   ├── templates/           # HTML templates for accounts app
│   ├── tests.py             # Unit tests
│   ├── urls.py              # URLs routing for accounts app
│   └── views.py             # View functions for accounts
├── blog/                    # Medical blog app for doctor and patient posts
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── migrations/          # Database migrations
│   ├── models.py            # Blog post models with categories and draft
│   ├── tests.py             # Blog app tests
│   └── views.py             # Views for blog functionality
├── manage.py                # Django management script
├── media/                   # Uploaded media files
│   └── blog_images/         # Images uploaded in blog posts
└── requirements.txt         # Python dependencies


```

## 🎯 Usage

### User Registration
1. Navigate to `/signup/`
2. Fill in all required information
3. Select user type (Patient or Doctor)
4. Upload profile picture (optional)
5. Submit form

### User Login
1. Navigate to `/login/` or `/`
2. Enter username or email
3. Enter password
4. System redirects based on role:
   - Patients → `/patient_dashboard/`
   - Doctors → `/doctor_dashboard/`

### Dashboards
- **Patient Dashboard**: Shows patient information and available features
- **Doctor Dashboard**: Shows doctor information and medical portal features
- **Logout**: Available from any dashboard

## 🔒 Security Features

- Password validation and confirmation
- CSRF protection on all forms
- Login required decorators on protected views
- Unique email and username validation
- Secure file upload handling

## 📸 Screenshots

### Signup Page
Clean, responsive registration form with role selection.

### Login Page
Simple login interface supporting username or email.

### Patient Dashboard
Patient-focused interface showing personal information and available features.

### Doctor Dashboard
Doctor-focused interface with medical portal features.

## 🛡️ User Roles

### Patient
- Personal health information management
- Appointment scheduling access
- Medical record viewing
- Communication with healthcare providers
-browse published posts by category


### Doctor
- Patient management capabilities
- Medical record access and updates
- Prescription management
- Patient communication tools
-create/edit blog posts with draft option and categories

## 🔧 Customization

The application is built with modularity in mind:

- **Models**: Easily extend the CustomUser model
- **Templates**: Raw HTML/CSS for easy styling customization
- **Views**: Function-based views for straightforward modification
- **Forms**: Django forms with built-in validation

## 📝 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Login page (home) |
| `/signup/` | GET/POST | User registration |
| `/login/` | GET/POST | User authentication |
| `/logout/` | GET | User logout |
| `/patient_dashboard/` | GET | Patient dashboard (protected) |
| `/doctor_dashboard/` | GET | Doctor dashboard (protected) |
| `/admin/` | GET | Django admin interface |

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

Created with ❤️ for healthcare authentication systems.

## 🆘 Support

If you encounter any issues or have questions:

1. Review the Django documentation
2. Check the terminal for error messages
3. Open an issue on GitHub

## 🔄 Version History

- **v1.0.0** - Initial release with core authentication features
  - User registration and login
  - Role-based dashboards
  - Profile picture uploads
  - Local development ready

---

**Note**: This is a demo application designed for local development and learning purposes.
