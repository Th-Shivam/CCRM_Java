# 🎓 CCRM Usage Guide

> **Complete step-by-step guide to using the CCRM Student Management System**

---

## 🚀 Quick Start

### ⚡ 1. Compile & Run

Execute these commands in your terminal from the project root directory:

```bash
# Compile the application
javac -d out -sourcepath src src/edu/ccrm/Main.java

# Run with assertions enabled
java -ea -cp out edu.ccrm.Main
```

> **💡 Pro Tip:** The `-ea` flag enables assertions for input validation!

### 📋 2. Main Menu Options

Once the application starts, you'll see this menu:

```
┌─────────────────────────────────────┐
│         CCRM Main Menu              │
├─────────────────────────────────────┤
│  1. List All Students               │
│  2. List All Courses                │
│  3. Enroll Student in Course        │
│  4. Assign Grade to Student         │
│  5. Show Student Transcript         │
│  6. Import Data from Files          │
│  7. Create Backup                   │
│  9. Exit                            │
└─────────────────────────────────────┘
```

---

## 📖 Common Workflows

### 🏁 First Time Setup

> **Start here if you're running the application for the first time**

| Step | Action | Command | Purpose |
|------|--------|---------|---------|
| 1️⃣ | **Import Data** | Enter `6` | Load student and course data from CSV files |
| 2️⃣ | **Verify Students** | Enter `1` | Check that student data loaded correctly |
| 3️⃣ | **Verify Courses** | Enter `2` | Confirm course data is available |

### 👨‍🎓 Enroll & Grade Students

> **Core workflow for managing student enrollments and grades**

#### 📝 Enrollment Process
1. **Start Enrollment** → Enter `3`
2. **Provide Student ID** → `23BCY10044`
3. **Provide Course Code** → `CSE1001`
4. **Confirm** → Student is now enrolled!

#### 📊 Grading Process
1. **Start Grading** → Enter `4`
2. **Student ID** → `23BCY10044`
3. **Course Code** → `CSE1001`
4. **Grade** → `A` (or `S`/`B`/`C`/`F`)

#### 🎯 View Results
1. **Show Transcript** → Enter `5`
2. **Student ID** → `23BCY10044`
3. **Review** → View grades and calculated GPA

---

## 📊 Sample Data Reference

### 👥 Sample Students
| Student ID | Name | Program |
|------------|------|---------|
| `23BCY10044` | Shivam Singh | B.Tech CSE |
| `23BCY10023` | Kapil Sharma | B.Tech CSE |
| `23BCY10056` | Priya Patel | B.Tech IT |

### 📚 Sample Courses
| Course Code | Course Name | Credits |
|-------------|-------------|---------|
| `CSE1001` | Introduction to Programming | 4 |
| `MA2001` | Calculus I | 3 |
| `PH1001` | Physics I | 4 |
| `ENG1001` | Technical English | 2 |

### 🎖️ Grading System
| Grade | Points | Description |
|-------|--------|-------------|
| **S** | 10.0 | Outstanding |
| **A** | 9.0 | Excellent |
| **B** | 8.0 | Very Good |
| **C** | 7.0 | Good |
| **F** | 0.0 | Fail |

---

## 💾 Backup System

### 📁 Creating Backups

1. **Manual Backup** → Enter `7`
2. **Automatic Naming** → System creates timestamped folder
3. **Location** → `backups/backup_YYYY-MM-DD_HH-MM-SS/`

### 📂 Backup Structure
```
project-root/
├── backups/
│   ├── backup_2024-03-15_14-30-45/
│   │   ├── students.csv
│   │   └── courses.csv
│   └── backup_2024-03-15_16-22-10/
│       ├── students.csv
│       └── courses.csv
```

---

## 🔄 Complete Example Workflow

### Scenario: New Student Registration & Grading

```bash
# 1. Start the application
java -ea -cp out edu.ccrm.Main

# 2. Menu Interactions
[6] Import Data from Files
    → "Data imported successfully!"

[1] List All Students  
    → Verify "23BCY10044 - Shivam Singh" appears

[2] List All Courses
    → Verify "CSE1001 - Introduction to Programming" appears

[3] Enroll Student in Course
    → Student ID: 23BCY10044
    → Course Code: CSE1001
    → "Student enrolled successfully!"

[4] Assign Grade to Student
    → Student ID: 23BCY10044
    → Course Code: CSE1001
    → Grade: A
    → "Grade assigned successfully!"

[5] Show Student Transcript
    → Student ID: 23BCY10044
    → View transcript with GPA calculation

[7] Create Backup
    → "Backup created at: backups/backup_2024-03-15_14-30-45/"

[9] Exit
    → "Thank you for using CCRM!"
```

---

## 🔧 Troubleshooting

### Common Issues & Solutions

| Issue | Solution |
|-------|----------|
| **"Student not found"** | Verify student ID exists using option `1` |
| **"Course not found"** | Check course code using option `2` |
| **"Invalid grade"** | Use only: `S`, `A`, `B`, `C`, or `F` |
| **"Already enrolled"** | Student cannot enroll in same course twice |
| **Compilation errors** | Ensure JDK 17+ is installed |

### 💡 Pro Tips

- ✅ **Always import data first** using option `6`
- ✅ **Use exact case** for student IDs and course codes
- ✅ **Create backups regularly** before major changes
- ✅ **Check transcripts** to verify GPA calculations
- ✅ **Enable assertions** with `-ea` flag for better validation

---

## 📱 Menu Navigation Tips

### Keyboard Shortcuts
- **Number + Enter** → Select menu option
- **9 + Enter** → Quick exit
- **Ctrl + C** → Force quit (if needed)

### Best Practices
1. 🔄 **Always verify data** after imports
2. 📋 **Keep student/course lists handy** for reference
3. 💾 **Backup before bulk operations**
4. 📊 **Check transcripts** after grade assignments
5. 🚪 **Exit gracefully** using option `9`

---

<div align="center">

**🎓 Happy Learning with CCRM!**  
*Built for efficient student management*

</div>
