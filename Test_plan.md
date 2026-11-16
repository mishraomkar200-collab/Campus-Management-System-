Campus Management System Test Plan
Fill Actual Result and Status after local execution.
ID
Test
Input/steps
Expected
Actual
Status
ST-01
Register student
Provide valid profile
New unique ID assigned
To record
Pending
ST-02
Blank name
Submit empty name
Registration rejected
To record
Pending
ST-03
Search existing student
Search sample ID 1001
Profile displayed
To record
Pending
ST-04
Search unknown ID
Search missing ID
Not found
To record
Pending
ST-05
Update profile
Change name/email
Changes persist
To record
Pending
ST-06
Remove enrolled student
Attempt remove ID enrolled in course
Removal blocked
To record
Pending
CO-01
Create course
Add valid course
ID assigned
To record
Pending
CO-02
Enroll valid pair
Existing student/course
Enrollment succeeds
To record
Pending
CO-03
Duplicate enrollment
Enroll same pair again
Duplicate denied
To record
Pending
CO-04
Capacity limit
Fill course, enroll extra student
Capacity denied
To record
Pending
CO-05
Remove enrollment
Remove existing relationship
Enrollment and result removed
To record
Pending
RE-01
Enter marks
Enrolled student; marks 0–100
Grade stored
To record
Pending
RE-02
Non-enrolled marks
Try marks for non-enrollment
Rejected
To record
Pending
RE-03
Invalid marks
Enter -1 or 101
Rejected
To record
Pending
RE-04
Grade boundary
Check marks 39,40,50,60,70,80,90,100
F,D,C,B,A,A+,O,O
To record
Pending
RE-05
Marksheet
Query student with results
Course, marks, grade displayed
To record
Pending
RE-06
Ranking
Generate ranking
Results in descending marks order
To record
Pending
LB-01
Add book
Enter title and copy count
Inventory item created
To record
Pending
LB-02
Issue available copy
Valid student/book and dates
Loan created; available count decreases
To record
Pending
LB-03
Issue unavailable book
Choose zero-copy item
Waiting queue request added
To record
Pending
LB-04
Return active loan
Loan ID and return date
Loan returned; copy count increases
To record
Pending
LB-05
Invalid return
Unknown or already-returned loan
Rejected
To record
Pending
LB-06
Duplicate active loan
Same student/book active
Rejected
To record
Pending
RP-01
Overdue report
Supply today date after due date
Active overdue loan listed
To record
Pending
DS-01
Merge Sort
Sort students by name
Names ascending
To record
Pending
DS-02
Binary Search
Search existing ID after sorting
Record found
To record
Pending
DS-03
Binary Search missing
Search unknown ID
Not found
To record
Pending
FI-01
Persistence
Save, exit, relaunch
Data reloads
To record
Pending
FI-02
Missing file
Temporarily move data file
App starts without crashing
To record
Pending
FI-03
Malformed row
Add invalid row to file
Row skipped
To record
Pending
IN-01
Numeric menu validation
Enter non-numeric/range error
Prompt repeats
To record
Pending
Demo flow
Register student → create course → enroll → marks entry → marksheet/ranking → add book → issue and return → reports → Merge Sort and Binary Search → save and relaunch.