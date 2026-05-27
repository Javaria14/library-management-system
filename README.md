# Library Management System

A CLI-based library management system written in C++ with dual login (Admin / Student), book issuance, fine calculation, and persistent file storage.

---

## Features

**Admin**
- Add, edit, and remove books
- View all books with availability and shelf position
- View all students sorted by roll number
- Check individual student balance

**Student**
- Create account (min $50 deposit, $50 registration fee deducted)
- View balance
- Deposit funds
- Issue a book (costs $2, one book at a time)
- Return a book (auto fine calculated if overdue)

---

## Fine & Issuance Policy

| Rule | Value |
|---|---|
| Issue period | 7 days |
| Issuance fee | $2.00 |
| Fine per overdue day | $1.00 |
| Min account deposit | $50.00 |

Fine is automatically deducted from the student's balance on return.

---

## Data Persistence

On every add, edit, deposit, issue, or return — data is saved automatically to two files:

- `students.txt` — roll number, name, balance, issued book index, issue date
- `books.txt` — title, author, ISBN, availability, due date, shelf position (row & column)

---

## How to Run

```bash
# Compile
g++ -o library projectcpp-103-javaria.cpp

# Run
./library
```

**Default password for both Admin and Student login:** `password`

---

## Project Structure

```
├── projectcpp-103-javaria.cpp   # Main source file
├── students.txt                 # Auto-generated on first save
└── books.txt                    # Auto-generated on first save
```

---

## Concepts Used

- Arrays & parallel arrays for data storage
- File I/O (`fstream`) for persistence
- `ctime` for issue date and fine calculation
- Bubble sort for student display by roll number
- Modular design with separate functions for each feature

---

## Author

Javaria Akbar| Bahria University, CS Semester 4
