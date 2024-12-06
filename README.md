# University Student Records Management System

## Project Overview
The *University Student Records Management System* is a robust application designed to manage university operations, including student enrollment, faculty records, course management, and academic performance tracking. Developed using *Visual C++* on the Microsoft Visual Studio platform, the system features a Multiple Document Interface (MDI) with intuitive menus and tools for seamless user interaction.

## Features
### Functional Features:
1. *User Authentication and Authorization*
   - Secure login with role-based access control.
   - Password reset and recovery options.

2. *Student Management*
   - Enroll in courses and view enrollment history.
   - View grades and transcripts.

3. *Faculty Management*
   - Enter, edit, and submit student grades.
   - Access and manage class rosters.

4. *Course Management*
   - Create and update course materials.
   - Manage course prerequisites and schedules.

5. *Academic Records*
   - Generate and print transcripts.
   - Audit and report academic performance.

### Non-Functional Features:
- *Scalability*: Supports up to 10,000 concurrent users.
- *Performance*: Page load time under 3 seconds during peak usage.
- *Security*: Data encryption and two-factor authentication.
- *Accessibility*: Compliance with WCAG 2.1 standards for user interfaces.
- *Reliability*: 99.9% uptime with backups and recovery within 1 hour.

## System Design
### Key Classes:
1. *User (Abstract Class)*
   - Attributes: userID, firstName, lastName, email, password.
   - Methods: login(), logout().

2. *Student (Inherits from User)*
   - Attributes: studentID, dateOfBirth, major, enrollmentDate.
   - Methods: enrollInCourse(), viewGrades().

3. *Faculty (Inherits from User)*
   - Attributes: facultyID, department, coursesTaught.
   - Methods: enterGrades(), viewRoster().

4. *Course*
   - Attributes: courseID, courseName, credits, schedule.
   - Methods: assignFaculty(), registerStudent().

5. *Enrollment*
   - Attributes: enrollmentID, studentID, courseID, semester, grade.
   - Methods: getEnrollmentDetails().

### Use Cases:
1. *Student*
   - Enroll in courses, view grades, access profiles, and pay fees.
2. *Faculty*
   - Manage courses, enter grades, and view rosters.
3. *Administrator*
   - Manage student and faculty data, oversee courses, and generate reports.

### Sequence Diagram
Example: Student Course Enrollment
1. Student initiates enrollInCourse().
2. System checks course availability.
3. If available, course data is updated with enrollment.
4. System confirms enrollment to the student.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Student-Records-Management.git
