# Study-planner
# 🧠 Study Planner & Reminder System

## 📌 Project Overview

This project is a **Python-based Study Planner and Reminder System** designed to help students organize their daily study tasks effectively.

It allows users to add study tasks, track completion status, and view pending work.

---

## 🎯 Objectives

* To help students manage study time efficiently
* To track completed and pending tasks
* To improve productivity and planning

---

## 🛠️ Technologies Used

* Python
* VS Code

---

## ⚙️ Features

* Add study tasks (subject, topic, time)
* View all tasks
* Mark tasks as completed
* View pending tasks
* Simple menu-driven interface

---

## ▶️ How to Run

```bash
python main.py
```

---

## 🧪 Sample Output

```
📚 Study Tasks:
1. Maths - Integration at 5PM [Pending]
```

---

## 🌱 Future Enhancements

* Add reminder notifications
* Store data using files
* Add deadline alerts
* Create GUI using Tkinter

---
PROGRAM:
```
# Study Planner & Reminder System

tasks = []

def add_task():
    subject = input("Enter subject: ")
    topic = input("Enter topic: ")
    time = input("Enter study time (e.g., 5PM): ")

    task = {
        "subject": subject,
        "topic": topic,
        "time": time,
        "status": "Pending"
    }

    tasks.append(task)
    print("✅ Task added successfully!")


def view_tasks():
    if not tasks:
        print("No tasks available.")
        return

    print("\n📚 Study Tasks:")
    for i, task in enumerate(tasks, start=1):
        print(f"{i}. {task['subject']} - {task['topic']} at {task['time']} [{task['status']}]")

        
def mark_completed():
    view_tasks()
    if not tasks:
        return

    try:
        num = int(input("Enter task number to mark complete: "))
        tasks[num-1]["status"] = "Completed"
        print("✅ Task marked as completed!")
    except:
        print("Invalid choice!")


def show_pending():
    print("\n⏳ Pending Tasks:")
    found = False
    for task in tasks:
        if task["status"] == "Pending":
            print(f"{task['subject']} - {task['topic']} at {task['time']}")
            found = True

    if not found:
        print("No pending tasks 🎉")


def main():
    while True:
        print("\n🧠 Study Planner System")
        print("1. Add Task")
        print("2. View All Tasks")
        print("3. Mark Task as Completed")
        print("4. View Pending Tasks")
        print("5. Exit")

        choice = input("Enter choice: ")

        if choice == '1':
            add_task()
        elif choice == '2':
            view_tasks()
        elif choice == '3':
            mark_completed()
        elif choice == '4':
            show_pending()
        elif choice == '5':
            print("Exiting program...")
            break
        else:
            print("Invalid choice!")


# Run program
main()
```
OUTPUT:

<img width="544" height="277" alt="Screenshot 2026-03-24 190225" src="https://github.com/user-attachments/assets/d3f3eacd-0654-40c3-95f7-b8f1f8265f33" />

## 📊 Result

The system successfully helps users plan and manage their study schedule.
It improves productivity by tracking completed and pending tasks.

---


