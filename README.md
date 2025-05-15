# 🎓 Exams Schedule Generator Using Genetic Algorithm
---
## 📌 Project Overview

This project implements a **Genetic Algorithm (GA)** from scratch in Python to generate a valid and optimized university **exam schedule**. The system ensures all hard constraints are strictly enforced while attempting to satisfy multiple soft constraints to enhance the usability and efficiency of the exam timetable.

---

## 🧮 Genetic Algorithm Components

The solution was built **from scratch** without using any pre-built GA libraries. The following GA components are implemented:

- **Population Initialization**
- **Fitness Function**
- **Roulette Wheel Selection**
- **Crossover (custom strategy used, see report for reasoning)**
- **Mutation (with controlled mutation rate)**
- **Generation Loop with Fitness Evaluation**

---

## 🧪 Fitness Function

The fitness function is designed to:
- Penalize schedules that **violate essential (hard) constraints**
- Reward schedules that **satisfy optimization (soft) criteria**

### ✔️ Hard Constraints (Must be satisfied):
1. Every course must have a scheduled exam.
2. No student should have overlapping exams.
3. Exams must be scheduled only on weekdays (Mon–Fri).
4. Exams must be held between 9 AM and 5 PM.
5. Each exam must have a unique invigilator.
6. Teachers must not invigilate back-to-back exams.

### ⭐ Soft Constraints (Improve fitness if satisfied):
1. Common break on Friday from 1–2 PM for all.
2. Avoid back-to-back exams for students.
3. Schedule MG exams before CS exams for students enrolled in both.
4. Two-hour break weekly for faculty meetings (split across two slots).

---

## 🗂️ Input Data

- Provided via **Excel files** containing:
  - Course info & codes
  - Teacher names
  - Student enrollments
  - Exam durations
  - Allowed classrooms (C301–C310)

---

## 📤 Output Format

The output is a **color-coded table** or **chart** showing:
- Day & time of each exam
- Course code
- Assigned classroom
- Invigilating teacher

Also includes:
- Fitness values of each generation
- Top 2–3 individuals per generation
- Summary of fulfilled constraints (both hard & soft)

---

## 📁 Repository Contents

| File Name                      | Description                                    |
|-------------------------------|------------------------------------------------|
| `examschedular.ipynb`        | Main Jupyter notebook with implementation     |
| `Report.pdf`          | Report detailing GA components and rationale  |
| `data/`                       | Contains sample Excel datasets                |
| `output/`                     | Generated timetables and visualizations       |
| `.gitattributes`              | (If using Git LFS for large files)            |
| `README.md`                   | This file                                     |

---

## ⚠️ Constraints

- No external GA libraries (only `NumPy`, `Pandas` allowed)
- Must implement **roulette wheel selection**
- Code must be well-documented and readable
  
---

## 🧑‍💻 Developed By

Tehreem Zafar


---
