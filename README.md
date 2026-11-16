Campus Management System
Major Project — C++17 with OOP and DSA
Overview
Menu-driven campus application for student administration, courses and enrollment, academic results and rankings, library inventory and loans, and reporting.
Requirements covered
Student registration, list, search by ID, update profile, controlled removal.
Course creation, list, enrollment, duplicate enrollment/capacity guards, enrollment report.
Marks entry for enrolled students only, range validation (0–100), grade policy, marksheets and ranking using a priority queue.
Library book inventory, issue and return, active-loan validation, overdue report.
Structures: vector, unordered_map indexes, queue waiting list, stack recent actions, priority_queue rankings.
Algorithms: implemented Merge Sort by student name and Binary Search by student ID (after ID sort).
Persistent text files in data/ folder.
Grade policy
Marks
Grade
90–100
O
80–89.99
A+
70–79.99
A
60–69.99
B
50–59.99
C
40–49.99
D
0–39.99
F
Structure
Campus_Management_System/
├── src/main.cpp
├── include/Entities.h
├── data/{students,courses,enrollments,results,books,loans}.txt
├── docs/Project_Report.pdf
├── test_cases/Test_Plan.md
├── screenshots/
├── README.md
└── .gitignore
Build and execute
Run from project root to ensure relative data paths resolve:
g++ -std=c++17 -Wall -Wextra -pedantic src/main.cpp -o campus_management
./campus_management
Windows: campus_management.exe.
Data integrity policies
IDs auto-increment beyond loaded highest ID (student starts 1001, course 501, book 201, loan 1).
Enrollment rejects unknown IDs, duplicates, and full courses.
Marks require an enrollment and must be between 0 and 100.
Student removal is prevented while associated course enrollments or active loans exist.
Pipe/newline characters in typed text are sanitized. Invalid file lines are skipped during load.
Waiting queue is in-memory for this project version and is not persisted.
Date fields require the YYYY-MM-DD shape; overdue report compares ISO dates lexicographically.
DSA complexity
Hash index ID lookup: average O(1), worst O(n).
Vector traversal: O(n); erase may shift O(n) items.
Merge Sort by name: O(n log n) time, O(n) extra space.
Binary Search by ID on sorted vector: O(log n); sorting beforehand costs O(n log n).
Priority queue: push/pop O(log n), top O(1).
Queue enqueue: O(1) typical; stack push/top: O(1).
Submission readiness
Compile and run tests locally, record actual test outcomes, take your own terminal screenshots, fill student details in report, create a public GitHub repository with meaningful commit history, and record the demo. Do not report tests as passed unless run.# Campus-Management-System-