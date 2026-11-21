 IMPORTANT NOTICE: The source code for this project has been lost. This repository serves as a documentation archive. It contains the complete academic internship report (PDF), architectural designs, and a detailed breakdown of the system's implementation as originally developed for El Fouladh. It is preserved here to showcase the system design, full-stack architecture, and engineering methodology applied during the internship.

 About the Project
 
Fouledh CMMS (Computerized Maintenance Management System) is a full-stack, real-time industrial solution designed for El Fouladh (Tunisian Steel Company), the sole integrated steel producer in Tunisia.

The system was built to replace manual, paper-based maintenance reporting with a digital workflow. It connects factory floor workers, supervisors, maintenance technicians, and administrators through a unified platform consisting of a Flutter mobile app and a web-based admin dashboard, all powered by a FastAPI backend.

 The Problem
 
In traditional factory settings, machine breakdowns are reported via phone calls, paper forms, or word of mouth. This causes:

Delays in notifying the right maintenance staff.

Lost information and lack of visibility into repair progress.

No centralized way to track which machines are down.

 The Solution
 
A multi-platform system that digitizes the entire ticket lifecycle:

Employees: Report breakdowns instantly from the factory floor via a mobile app (with photo upload and priority setting).

Supervisors: Receive real-time notifications, acknowledge tickets, and assign them to technicians.

Maintenance Technicians: Track assigned tickets, start repairs, and mark them as resolved.

Admins: Monitor the entire plant via a web dashboard, manage users (approve/reject supervisor accounts), oversee machine network status, and view full audit trails.

 Technical Architecture & Stack
 
The system was developed during a one-month internship using Scrum methodology across four sprints.

Backend: Python, FastAPI, Uvicorn

Database: MySQL 8.x

Mobile App: Flutter (Dart), compiled to Android APK

Admin Dashboard: Vanilla HTML, CSS, JavaScript (Dark-themed, no framework overhead)

Real-Time Communication: WebSockets (Custom Hub for live ticket and user updates)


Authentication & Security: JWT (JSON Web Tokens), bcrypt password hashing, Admin approval workflow for sensitive roles.

Infrastructure: Runs entirely on the plant's Local Area Network (LAN/Wi-Fi). No cloud dependency. A background scheduler (APScheduler) pings machine IPs to monitor network status (Online/Offline/Unreachable).

 Core Entities (Data Model)
 
Section: The three maintenance areas of the plant (Steelmaking, Rolling, Wire-rod).

User: Distinguishes between Employee, Supervisor, Technician, and Admin. Includes approval status.

Machine: Tracks equipment status and IP connectivity.

Ticket: The core workflow object (Reported → Acknowledged → In Progress → Resolved).

TicketEvent: An audit trail logging every single status change with timestamps and the acting user.

 What's Inside This Repository
 
 Fouledh_Maintenance_App_Report.pdf: The complete, official internship report submitted to IMSET and El Fouladh. It includes full use case diagrams, class diagrams, sprint backlogs, and physical architecture diagrams.

 README.md: This document.

 My Contributions & Scope
 
As an individual intern (Second Year, Web Development Program at IMSET under the supervision of Mrs. Aness Bouaoud and Mr. Iheb Nefzi), I designed and developed the entire system from scratch. My work included:

Designing the MySQL schema and building the FastAPI REST endpoints.

Implementing the JWT authentication system and the custom WebSocket hub for real-time dashboard updates.

Developing the Flutter mobile application, including offline ticket creation and auto-sync logic.

Building the vanilla JS admin dashboard for real-time monitoring.

Setting up the background APScheduler to ping machine IPs and update their network status.

Conducting end-to-end integration testing across all three components.

 Why the Source Code is Missing
 
This project was developed and completed entirely on my local machine during the academic year. I had not yet pushed it to a remote repository (GitHub or any other backup service), which turned out to be a costly oversight.

Shortly after the project's completion, my computer was stolen. Despite my efforts, the device was never recovered, and with it I lost the project's source code along with several other personal projects I had been developing locally.

This repository serves as a record of the work that was done. The attached academic report contains the full documentation of the design, architecture, and implementation, and stands as evidence of the project's scope and the engineering effort behind it.

I now maintain a strict habit of pushing all work to GitHub from the first day of any project and keeping regular remote backups.

 See Also
 
Kumkim: Desktop Companion AI — My other archived project, featuring a 11,000-line Python autonomous AI companion.

My active projects — Check out my latest real-time full-stack web applications (React + TypeScript + Supabase).

Note: If you are a recruiter or developer reviewing this, feel free to read the attached PDF report to see the detailed sequence diagrams, class architectures, and sprint planning that went into this full-stack industrial system.

[fouledth maintenance app.pdf](https://github.com/user-attachments/files/35215811/fouledth.maintenance.app.pdf)


