# 📚 Course Prerequisite Checking System

## 📌 Project Overview

This project simulates a course registration system that checks whether a student is eligible to register for specific courses based on completed prerequisites.

The system handles both direct and indirect prerequisites using a binary tree structure, ensuring that all prerequisite dependencies are satisfied before allowing course registration.

> 📄 **Important Note:**
> The repository includes a PDF file named **“Courses and Prerequisites”** inside the `docs/` folder.
> This file contains visual illustrations of the prerequisite trees used in this project and helps explain how course dependencies are structured and traversed.

---

## 🧠 Problem Statement

Students may attempt to register for courses without satisfying all prerequisite requirements, especially when prerequisites involve multiple dependency levels.

This project prevents invalid registration attempts by automatically validating all prerequisite chains before registration.

---

## 🛠️ Concepts & Data Structures Used

* **Linked Lists**

  * Store all courses loaded from the CSV file.

* **Binary Trees**

  * Represent prerequisite dependency relationships between courses.

* **Recursion**

  * Traverse and validate prerequisite trees.

* **File I/O**

  * Read course information from `courses.csv`.

---

## 📂 Repository Structure

```bash
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
```

---

## 📄 CSV File Format (`courses.csv`)

Each line in the CSV file represents a course:

```csv
course_code,course_name,prerequisite1,prerequisite2
```

Use `-1` if a course has no prerequisite.

### Example

```csv
CS101,Introduction to Programming,-1,-1
CS102,Data Structures,CS101,-1
CS201,Algorithms,CS102,MA101
```

---

## ⚙️ How the Program Works

1. Reads course data from `courses.csv`
2. Builds a linked list containing all available courses
3. Accepts user input:

   * Completed courses
   * Desired courses
4. Removes invalid desired course codes
5. Builds a prerequisite tree for each desired course
6. Recursively checks eligibility
7. Displays:

   * Courses the student **can register for**
   * Courses the student **cannot register for** due to missing prerequisites

---

## ▶️ How to Compile & Run

### Compile

```bash
gcc main.c -o course_checker
```

### Run

```bash
./course_checker
```

> 📌 Make sure `courses.csv` is in the same directory as the executable or update the file path accordingly.

---

## 🌳 Example Features

* Handles multi-level prerequisites
* Detects indirect dependency chains
* Uses recursive tree traversal
* Filters invalid course codes
* Visualizes prerequisite structures

---

## 🎯 Learning Outcomes

This project demonstrates practical usage of:

* Dynamic memory allocation in C
* Linked lists
* Binary trees
* Recursive algorithms
* Modular programming
* File handling in C
* Data validation techniques

---

## 👨‍💻 Author

Developed as a Data Structures project to simulate real-world course prerequisite validation systems.
