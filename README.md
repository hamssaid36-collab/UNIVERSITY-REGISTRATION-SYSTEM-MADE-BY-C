📚 Course Prerequisite Checking System
📌 Project Overview
This project simulates a course registration system that checks whether a student is eligible to register for specific courses based on completed prerequisites.

The system handles direct and indirect prerequisites using a binary tree, ensuring that all prerequisite dependencies are satisfied before allowing registration.

📄 Important Note: The repository includes a PDF file named “Courses and Prerequisites” that contains visual illustrations of the prerequisite trees used in this project. Please refer to this file to better understand how course dependencies are structured and traversed.

🧠 Problem Statement
Students may attempt to register for courses without meeting all prerequisite requirements, especially when prerequisites are multi-level and dependent on each other.

This project prevents incorrect registration by validating all prerequisite chains automatically.

🛠️ Concepts & Data Structures Used
Linked Lists: Store all courses read from a CSV file
Binary Trees: Represent prerequisite dependency relationships
Recursion: Traverse and validate prerequisite trees
File I/O: Read course data from courses.csv
📂 Repository Structure
Course-Prerequisite-Checking-System/
│
├── src/
│   ├── main.c
│   ├── courses.c
│   ├── build_tree.c
│   ├── eligibility.c
│   ├── is_completed.c
│   ├── find_node.c
│   ├── Course_list_build.c
│   ├── Displaylist.c
│   ├── printInorder.c
│   ├── printTreevisual.c
│   ├── validate_courses.c
│
├── include/
│   ├── courses.h
│   ├── build_tree.h
│   ├── eligibility.h
│   ├── is_completed.h
│   ├── find_node.h
│   ├── Course_list_build.h
│   ├── Displaylist.h
│   ├── printInorder.h
│   ├── printTreevisual.h
│   ├── validate_courses.h
│   ├── structs_.h
│
├── data/
│   ├── courses.csv
│
├── docs/
│   ├── Courses and Prerequisites.pdf
│
├── README.md
📄 CSV File Format (courses.csv)
Each line represents a course:

course_code,course_name,prerequisite1,prerequisite2
Use -1 if a course has no prerequisite.
⚙️ How the Program Works
Reads course data from courses.csv

Builds a linked list of all available courses

Takes user input:

Completed courses
Desired courses
Removes invalid desired course codes

Builds a prerequisite tree for each desired course

Checks eligibility using recursion

Displays:

Courses the student can register for
Courses the student cannot register for (missing prerequisites)
▶️ How to Compile & Run
Compile
gcc main.c -o course_checker
Run
./course_checker
📌 Make sure courses.csv is in the same directory as the executable.
