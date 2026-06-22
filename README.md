🏥 ClinicQueue Management System

A comprehensive Clinic Queue Management System built with Python and Tkinter. This application helps healthcare facilities manage patient queues, doctor assignments, and patient flow efficiently.
📋 Table of Contents

    Features

    Screenshots

    Installation

    Usage

    User Guide

    Technical Details

    Project Structure

    Contributing

    License

✨ Features
🔐 Authentication

    User Login - Secure login with email and password

    User Registration - Create new accounts with name, email, and password

    Session Management - Persistent user sessions

    Demo Accounts - Pre-configured accounts for testing

📊 Dashboard

    Real-time Statistics - Total patients, waiting, in-progress, and completed

    Now Serving Display - Clearly shows current patient being served

    Queue List - Scrollable list of all waiting patients with priority indicators

    Doctor Status - Real-time view of doctor availability and patient load

➕ Patient Check-in

    Patient Registration - Add new patients to the queue

    Priority Levels - Urgent, High, Normal, Low

    Department Selection - Cardiology, Orthopedics, Dermatology, Neurology, Pediatrics, ENT, Ophthalmology, General

    Doctor Assignment - Assign patients to specific doctors

    Phone & Notes - Optional patient information fields

🎫 Queue Management

    Queue Table View - Comprehensive table of all patients

    Status Updates - Mark patients as In Progress, Completed, or Cancelled

    Right-click Menu - Quick actions on individual patients

    Bulk Actions - Clear all completed patients

    Priority Tags - Visual indicators for urgent and high-priority patients

👨‍⚕️ Doctor Management

    Doctor Profiles - View all doctors with specialties and room numbers

    Status Toggle - Switch doctors between Available and Busy

    Patient Count - See how many patients are assigned to each doctor

    Real-time Updates - Doctor status updates automatically

🔄 Auto-Refresh

    Live Updates - Dashboard refreshes every 5 seconds

    Queue List - Automatically updates without page reload

    Now Serving - Real-time display of current patient

🚀 Installation
Prerequisites

    Python 3.7 or higher

    Tkinter (usually comes pre-installed with Python)

Steps

    Clone the repository

bash

git clone https://github.com/yourusername/clinic-queue-system.git
cd clinic-queue-system

    Run the application

bash

python clinic_queue_system.py

No additional dependencies required!

The application uses only Python's standard library (tkinter, json, os, datetime).
💻 Usage
Default Accounts
Email	Password	Role
admin@clinic.com	admin123	Administrator
doctor@clinic.com	doctor123	Doctor
Quick Start

    Login using the default credentials or create a new account

    Dashboard view shows the current state of the clinic

    Check-in patients using the dedicated form

    Manage Queue through the queue management panel

    Monitor Doctors status in real-time

📖 User Guide
Login Screen

https://screenshots/login.png

    Enter your email and password

    Click "Sign in" or press Enter

    Use "Sign up" to create a new account

Dashboard

https://screenshots/dashboard.png

The dashboard is divided into three sections:
Left Panel - Now Serving

    Displays the current patient being served

    Shows ticket number, name, doctor, department, and priority

    "Next Patient" button to move to the next waiting patient

    "Complete" button to finish current patient

Center Panel - Queue List

    Scrollable list of all waiting patients

    Color-coded priority indicators:

        🟥 Urgent

        🟨 High

        🟦 Normal

        ⬜ Low

    Status badges show current status

Right Panel - Doctor Status

    Real-time doctor availability

    Patient count per doctor

    Status indicators (🟢 Available / 🟡 Busy)

Patient Check-in

    Navigate to "Check-in Patient" tab

    Fill in patient details:

        Name (required)

        Phone (optional)

        Priority (Urgent/High/Normal/Low)

        Department (Select from list)

        Doctor (Select from list)

        Notes (Optional)

    Click "Check-in Patient"

    Patient receives a unique ticket number

Queue Management

    Navigate to "Queue Management" tab

    View all patients in a table format

    Right-click on any patient to:

        Mark as "In Progress"

        Complete patient

        Cancel patient

        Remove from queue

    Use "Clear Completed" to remove all completed patients

Doctor Management

    Navigate to "Doctors" tab

    View all doctors with their details

    Toggle doctor status between "Available" and "Busy"

    See patient count per doctor

🛠️ Technical Details
Architecture
text

┌─────────────────────────────────────────────────────────────┐
│                    ClinicQueue Management System              │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   Login      │  │   Signup    │  │   Dashboard         │ │
│  │   Screen     │  │   Screen    │  │   (Auto-refresh)    │ │
│  └─────────────┘  └─────────────┘  └─────────────────────┘ │
│                                                               │
│  ┌─────────────────────────────────────────────────────────┐ │
│  │                    Main Features                        │ │
│  │  ┌────────────┐  ┌────────────┐  ┌─────────────────┐  │ │
│  │  │ Check-in   │  │   Queue    │  │    Doctors      │  │ │
│  │  │ Patient    │  │ Management │  │   Management    │  │ │
│  │  └────────────┘  └────────────┘  └─────────────────┘  │ │
│  └─────────────────────────────────────────────────────────┘ │
│                                                               │
│  ┌─────────────────────────────────────────────────────────┐ │
│  │                  Data Layer                             │ │
│  │  ┌────────────┐  ┌────────────┐  ┌─────────────────┐  │ │
│  │  │  Users     │  │   Queue    │  │    Doctors      │  │ │
│  │  │  (JSON)    │  │   (List)   │  │    (List)       │  │ │
│  │  └────────────┘  └────────────┘  └─────────────────┘  │ │
│  └─────────────────────────────────────────────────────────┘ │
│                                                               │
└─────────────────────────────────────────────────────────────┘

Data Storage

    Users: Stored in users.json file

        Email as key

        Password and name as values

        Auto-created if file doesn't exist

    Queue: In-memory list

        Patient information

        Status tracking

        Timestamps

    Doctors: Pre-configured list

        Name, specialty, room

        Status tracking

Key Classes & Methods
ClinicQueueManagementSystem

    __init__() - Initialize the application

    show_login() - Display login screen

    show_dashboard() - Display main dashboard

    show_checkin() - Display patient check-in form

    show_queue_management() - Display queue management

    show_doctors() - Display doctor management

    handle_checkin() - Process patient check-in

    next_patient() - Move to next patient

    complete_current() - Complete current patient

    auto_refresh() - Refresh dashboard every 5 seconds

📁 Project Structure
text

clinic-queue-system/
│
├── clinic_queue_system.py   # Main application file
├── users.json                # User data storage (auto-created)
├── README.md                 # This file
│
├── screenshots/              # Screenshot images
│   ├── login.png
│   ├── dashboard.png
│   ├── checkin.png
│   └── queue_management.png
│
└── docs/                     # Documentation
    ├── api.md
    └── user_guide.md

🎨 Color Scheme
Element	Color	Hex
Primary	Blue	#2563eb
Success	Green	#22c55e
Warning	Amber	#eab308
Danger	Red	#dc2626
Urgent	Red	#dc2626
High	Amber	#eab308
Normal	Blue	#2563eb
Low	Gray	#64748b
🤝 Contributing


git checkout -b feature/amazing-feature

Commit your changes
bash

git commit -m 'Add some amazing feature'

Push to the branch
bash

git push origin feature/amazing-feature



📝 License

This project is licensed under the MIT License - see the LICENSE file for details.
🙏 Acknowledgments

    Built with Python's Tkinter library

    Inspired by modern clinic management systems

    Designed for efficiency and ease of use

📞 Support

For support, email support@clinicqueue.com or create an issue on GitHub.

Made with ❤️ for healthcare providers
