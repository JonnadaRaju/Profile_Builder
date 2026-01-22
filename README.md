# Profile Builder 🚀

Profile Builder is an automated static website generator that creates **individual student portfolio websites** using a single HTML template and structured CSV data.

This project was built as part of my **backend learning journey at AI Karyashala**, inspired by a real-world requirement discussed during the **APDTS Summit**.

---

## 📌 Project Motivation

We had a batch of **30 students**, and manually creating professional profiles (GitHub, LinkedIn, projects, skills) for each student was:

- Time-consuming  
- Error-prone  
- Not scalable  

The objective was to **automate profile creation** using backend scripting and reusable templates.

---

## 🎯 Project Objective

- Automatically generate individual student portfolio websites  
- Use one reusable HTML template  
- Read student data from a CSV file  
- Create clean, organized output folders  
- Eliminate manual HTML duplication  

---

## 🛠️ Technologies Used

- Python (Automation & Scripting)
- HTML & CSS (Frontend Template)
- CSV (Structured Data Source)
- OS & CSV Python modules

---

## 📂 Project Structure

```
Profile-Builder/
│
├── generate_pages.py        
├── students.csv             
├── index.html               
├── assets/                  
│   ├── 101.jpeg
│   └── 102.jpeg
│
└── students_pages/          
    ├── 101/
    │   └── index.html
    ├── 102/
    │   └── index.html
    └── 103/
        └── index.html
```

---

## 📄 How It Works

1. **students.csv** stores student details such as:
   - `student_id`
   - `name`
   - `email`
   - `github`
   - `linkedin`
   - `projects`

2. **index.html** acts as a reusable template and contains placeholders like:
   ```
   {{name}}, {{email}}, {{github}}, {{linkedin}}, {{student_id}}
   ```

3. **generate_pages.py**:
   - Reads data from the CSV file  
   - Replaces placeholders in the HTML template  
   - Creates a separate folder for each student  
   - Generates a personalized `index.html` page  

---
## 🧪 Example Output

Below is an example of a generated student profile with QR code access:

![Student Profile Example](images/AIK073930_front.png)

---
## ▶️ How to Run the Project

### Step 1: Prepare CSV File

Ensure `students.csv` follows this format:

```csv
student_id,name,email,github,linkedin,projects
101,Raju Jonnada,raju@email.com,https://github.com/raju,https://linkedin.com/in/raju,https://github.com/raju?tab=repositories
```

---

### Step 2: Add Student Images

```
assets/
 └── 101.jpeg
 └── 102.jpeg
```

---

### Step 3: Run the Script

```bash
python generate_pages.py
```

---

### Step 4: View Generated Profiles

```
students_pages/<student_id>/index.html
```
