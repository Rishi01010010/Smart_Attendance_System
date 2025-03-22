# 📸 Smart Attendance System with Face Recognition 📸

Welcome to the *Smart Attendance System*, an innovative Python and Node.js-based solution that automates attendance tracking using facial recognition. Developed as a mini-project for Sai Vidya Institute of Technology, this system leverages advanced technologies like DeepFace, FaceNet, and MongoDB to streamline attendance management for educational institutions.

## 🛠️ Project Overview

The *Smart Attendance System* replaces traditional, error-prone attendance methods with a modern, automated approach. By uploading a single class photo, the system identifies students using facial recognition and generates an attendance report instantly. Built with a client-server architecture, it combines a responsive web interface, robust backend processing, and a scalable database to deliver efficiency and accuracy.

### ✨ Key Features:

- *Facial Recognition:* Uses DeepFace and FaceNet to detect and identify students from class photos with high accuracy.
- *Web-Based Interface:* A user-friendly frontend built with HTML, CSS, JavaScript, and EJS for managing students and attendance.
- *Real-Time Attendance:* Processes uploaded photos and marks attendance in seconds, storing results in MongoDB.
- *Scalable Database:* MongoDB stores student details and attendance records, supporting growth and flexibility.
- *Cross-Platform:* Runs on Windows or Linux systems with minimal setup.

## 🚀 Getting Started

### 1. *Prerequisites:*
- Python 3.x and Node.js installed on your system.
- MongoDB installed and running locally or on a server.
- A webcam or sample photos for testing (e.g., from the `classmates/` or `Sample_Photos/` directories).

### 2. *Setting Up:*

- Clone the repository:
  ```bash
  git clone https://github.com/Rishi01010010/Smart_Attendance_System.git
  cd Smart_Attendance_System
  ```

- Install Node.js dependencies:
  ```bash
  npm install
  ```

- Install Python dependencies (for facial recognition):
  ```bash
  pip install deepface opencv-python numpy
  ```

- Start MongoDB:
  ```bash
  mongod
  ```

- Run the server:
  ```bash
  node server.js
  ```

- Open your browser and navigate to `http://localhost:3000` to access the application.

### 3. *Using the System:*

- *Add Students:* Use the "Add Student" page to upload individual student photos and details.
- *Upload Class Photo:* Submit a group photo via the "Upload" page to mark attendance automatically.
- *View Attendance:* Check the attendance table on the "Attendance" page for real-time results.

### 4. *Sample Data:*

- Test with preloaded images in `classmates/` (e.g., `Abhi.jpeg`, `group.jpeg`) or `Sample_Photos/` (e.g., `Albert-Einstein.webp`).

## 💾 File Structure

```bash
Smart_Attendance_System/
│
├── backend/              # Backend debugging and temp files
│   ├── debug_A1.jpg
│   ├── debug_A2.jpg
│   └── student_image_temp.jpg
│
├── classmates/           # Sample student photos for testing
│   ├── Abhi.jpeg
│   ├── group.jpeg
│   └── [more student images]
│
├── frontend/             # Frontend assets and UI files
│   ├── index.html       # Landing page
│   ├── script.js        # Client-side JavaScript
│   ├── styles.css       # Styling for the web interface
│   └── [images: att.jpg, home.png, etc.]
│
├── models/               # MongoDB schema definitions
│   └── student.js       # Student schema for database
│
├── Sample_Photos/        # Additional sample images for testing
│   ├── Albert-Einstein.webp
│   ├── solvay.jpg
│   └── [more famous scientists]
│
├── uploads/              # Temporary storage for uploaded photos
│   ├── [hashed filenames, e.g., 0118e64345db8f23fee01d09cb914206]
│   └── [more uploaded images]
│
├── views/                # EJS templates for dynamic rendering
│   ├── home.ejs         # Home page template
│   ├── student.ejs      # Add student form
│   ├── stud_db.ejs      # Student list display
│   └── upload.ejs       # Photo upload page
│
├── face_recognition1.py  # Python script for facial recognition using DeepFace
├── server.js             # Main Node.js server with Express.js
├── mong.js               # MongoDB connection setup
├── package.json          # Node.js dependencies and scripts
├── test.html             # Test HTML file (for development)
├── test.js               # Test JavaScript (for development)
├── update.js             # Script for updating database records
└── use attendance.txt    # Attendance log file
```

### 📝 Code Explanation

1. *server.js*:
   - Sets up the Express.js server, handles routing, and integrates with MongoDB and Python scripts.
   - Manages file uploads and serves EJS templates.

2. *face_recognition1.py*:
   - Implements facial recognition using DeepFace and FaceNet, processing uploaded photos to identify students.
   - Outputs results to the server for attendance marking.

3. *mong.js*:
   - Establishes the MongoDB connection and defines database operations.

4. *frontend/script.js & styles.css*:
   - Handles client-side interactivity (e.g., form submissions) and styles the web interface.

5. *views/*.ejs*:
   - Dynamic templates for rendering the UI, including home, student management, and attendance pages.

## 🌐 System Configuration

- *Database:* Ensure MongoDB is running (`mongod`) and configured in `mong.js`.
- *Photo Quality:* Use well-lit, clear images for best recognition results.
- *Port:* Default port is 3000; modify in `server.js` if needed.

## 🛠️ How It Works

1. *Student Registration*: Add student details and photos via the web interface, stored in MongoDB and referenced in `classmates/`.
2. *Attendance Marking*: Upload a class photo; the system processes it with `face_recognition1.py`, matches faces, and updates the attendance in MongoDB.
3. *Results Display*: View the attendance table with present/absent statuses on the web interface.

## 🎯 Project Intent

Developed as a mini-project (BCS586) for Visvesvaraya Technological University, this system demonstrates the application of facial recognition, web development, and database management to solve real-world problems in education. It’s an excellent showcase of teamwork and technical skills by Abhinavaa S Kumar, Lakshmi Preksha, Risheek R, and Mohammed Shahid.

## 🔧 Customization

Enhance the project with these ideas:
- *Cloud Storage:* Integrate AWS S3 for photo storage instead of local `uploads/`.
- *GUI Upgrade:* Replace EJS with a modern framework like React for a richer UI.
- *Mobile App:* Develop a companion app for on-the-go attendance tracking.
- *Analytics:* Add attendance trends and insights using data from MongoDB.

Demo_Link: https://www.youtube.com/watch?v=hm01gw_WiKk&feature=youtu.be
