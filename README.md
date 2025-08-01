# CampusLink - A Centralized Student Utility Hub
PROJECT DESCRIPTION:
CampusLink is a web application designed to unify essential student services on a college campus into a single, easy-to-use platform. It centralizes communication through announcements, facilitates management of lost and found items, allows students to create and track their weekly class timetables, and enables hostel complaint registration with status updates. The system includes secure student and admin login with role-based access using Firebase Authentication. Additional features promote collaborative learning through a skill exchange marketplace, provide tech news and opportunities, and gather feedback via polls. Built with a Python backend, MongoDB database, and an HTML/CSS frontend, CampusLink aims to streamline campus life, improve accessibility, and enhance communication between students and administrators.
CampusLink is a comprehensive web application designed to streamline essential student services within a college campus, improving communication, accessibility, and daily productivity for both students and administrators.

**TECH STACK USED:**
Frontend: HTML, CSS (optionally React.js if SPA features are included)

Backend: Python (using Flask)

Database: MongoDB

Authentication & Security: Firebase Authentication

RESTful API communication between frontend and backend

**SETUP INSTRUCTIONS:**
Setup Instructions
Clone the Repository

bash
git clone https://github.com/yourusername/campuslink.git
cd campuslink
Install Backend Dependencies

Make sure you have Python installed.

Install dependencies (assuming requirements.txt exists):

bash
pip install -r requirements.txt
Frontend Setup

If using only HTML/CSS:

You can simply open frontend/index.html in your browser for static pages.

For integration with backend, move HTML/CSS files to your Flask or Django templates directory.

Database Setup

Ensure MongoDB is installed and running locally, or provide a connection string for a remote instance.

Update database configuration in your backend settings (usually in a .env file or the backend config file).

Configure Firebase Authentication

Set up a Firebase project at [firebase.google.com].

Enable Email/Password authentication (or any other provider you prefer).

Download your Firebase Admin SDK credentials and add them to your backend config.

Update your frontend/firebase.js or similar file with your Firebase project config.

Run the Backend Server

For Flask:

bash
python app.py


Access the Application

Open your browser and navigate to the frontend interface (usually http://localhost:5000 or http://localhost:8000).

Log in or sign up as a student or admin to begin using your application.

Optional: Cloud Storage for Images

Configure Firebase Storage or local storage in the backend for file uploads, if required.

Additional notes:

Modify environment variables and configuration files (.env) according to your environment (database URI, Firebase keys, server port, etc.).

For any changes in frontend or backend code, restart the backend server.

**TEAM MEMBERS**
ANAS F
POOJA S
SURYA PRAKASH S
PRATHEKSHA S


## Features

### Core Features
1. **Campus Announcements Feed** - Admin posts important updates like events, exams, holiday notices
2. **Lost & Found Section** - Students report or search for lost/found items with smart filters
3. **Mini Timetable Scheduler** - Students can input and manage their weekly class schedule
4. **Hostel Complaint Registration** - Raise and track complaints with status updates
5. **User Authentication System** - Student and admin login with role-based access

### Additional Features
6. **Skill Exchange Marketplace** - Students list skills they can teach and book peer learning sessions
7. **Tech News & Opportunities Feed** - Curated section for hackathons, internships, tech news
8. **Polls & Feedback** - Admins create polls and collect feedback from students

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Python Flask
- **Database**: MongoDB
- **Authentication**: Firebase (configurable)
- **Styling**: Custom CSS with responsive design

## Project Structure

```
CampusLink/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── static/
│   ├── css/
│   │   └── style.css     # Main stylesheet
│   ├── js/
│   │   └── main.js       # Common JavaScript functions
│   └── uploads/          # File upload directory
└── templates/
    ├── base.html         # Base template
    ├── index.html        # Landing page
    ├── login.html        # Authentication page
    ├── dashboard.html    # Main dashboard
    ├── announcements.html # Announcements page
    ├── lost_found.html   # Lost & Found page
    ├── timetable.html    # Timetable scheduler
    ├── complaints.html   # Complaints system
    ├── skills.html       # Skill exchange
    ├── news.html         # Tech news & opportunities
    └── polls.html        # Polls & feedback
```

## Installation & Setup

### Prerequisites
- Python 3.8 or higher
- MongoDB (local installation or MongoDB Atlas)
- Git

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd CampusLink
```

### Step 2: Create Virtual Environment
```bash
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: MongoDB Setup

#### Option A: Local MongoDB
1. Install MongoDB Community Edition
2. Start MongoDB service
3. The application will connect to `mongodb://localhost:27017/`

#### Option B: MongoDB Atlas (Cloud)
1. Create a MongoDB Atlas account
2. Create a new cluster
3. Get your connection string
4. Update the connection string in `app.py`

### Step 5: Firebase Setup (Optional)
1. Create a Firebase project
2. Generate service account credentials
3. Download the JSON file
4. Update the Firebase configuration in `app.py`

### Step 6: Run the Application
```bash
python app.py
```

The application will be available at `http://localhost:5000`

## Default Login Credentials

For testing purposes, you can use these credentials:
- **Student**: Any email with password (demo mode)
- **Admin**: Any email with role set to 'admin'

## API Endpoints

### Announcements
- `GET /api/announcements` - Get all announcements
- `POST /api/announcements` - Create new announcement (admin only)

### Lost & Found
- `GET /api/lost-found` - Get all lost/found items
- `POST /api/lost-found` - Report new item

### Timetable
- `GET /api/timetable?user_id=<id>` - Get user's timetable
- `POST /api/timetable` - Add/update timetable entry

### Complaints
- `GET /api/complaints` - Get all complaints
- `POST /api/complaints` - File new complaint
- `PUT /api/complaints` - Update complaint status (admin only)

### Skills
- `GET /api/skills` - Get all skills
- `POST /api/skills` - Offer new skill

### News
- `GET /api/news` - Get all news items
- `POST /api/news` - Add news item (admin only)

### Polls
- `GET /api/polls` - Get all polls
- `POST /api/polls` - Create new poll (admin only)
- `PUT /api/polls` - Vote on poll

## Features Overview

### For Students
- View campus announcements and news
- Report lost items or search for found items
- Manage personal class timetable
- File hostel complaints and track status
- Offer skills or book learning sessions
- Participate in polls and provide feedback
- Stay updated with tech opportunities

### For Administrators
- Post campus announcements
- Manage complaint status updates
- Create polls for feedback collection
- Add tech news and opportunities
- Monitor system usage and statistics

## Responsive Design

The application is fully responsive and works seamlessly on:
- Desktop computers
- Tablets
- Mobile phones

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## Security Features

- Input validation and sanitization
- CORS protection
- Secure session management
- Role-based access control
- XSS protection

## Performance Optimizations

- Lazy loading for images
- Debounced search functionality
- Efficient database queries
- Minified CSS and JavaScript
- Responsive image loading

## Future Enhancements

- Push notifications
- Mobile app development
- Advanced analytics dashboard
- Integration with college ERP systems
- Multi-language support
- Dark mode theme

## Troubleshooting

### Common Issues

1. **MongoDB Connection Error**
   - Ensure MongoDB is running
   - Check connection string
   - Verify network connectivity

2. **Port Already in Use**
   - Change port in `app.py`
   - Kill existing processes using the port

3. **Module Not Found Error**
   - Ensure virtual environment is activated
   - Reinstall requirements: `pip install -r requirements.txt`

4. **Static Files Not Loading**
   - Check file paths in templates
   - Ensure static folder structure is correct

## Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Flask community for excellent documentation
- MongoDB for reliable database services
- Font Awesome for beautiful icons
- Google Fonts for typography

---

**CampusLink** - Making campus life easier, one feature at a time! 🎓✨#   J a r v i s 
 
 
