# ATTENDANCE-PERFORMANCE-CALCULATOR
This is the simple python code which calculates a students attendance percentage based on the number of classes they attended out of the total classes conducted.

PROBLEM STATEMENT-: 
Many schools and colleges require a simple way to evaluate a student's attendance and understand how consistent they are in attending classs.
Therefore,a program is needed that can automatically calculate attendance percentage and provide a remark.

OBJECTIVE-:
1.To create a Python program that calculates a student’s attendance percentage accurately.
2.To generate a performance remark automatically based on the attendance percentage.
3.To help students and teachers quickly assess attendance performance without manual work.

FEATURES-:
1.Allows the user to enter the number of attended and total classes.
2.Prevents division by zero by checking if total classes are zero.
3.Automatic Percentage Calculation.

ALGORITHM-:
1. Start
2. Ask the user to enter attended classes.
3. Ask the user to enter total classes.
4.If total classes = 0, show a message:
“Total classes cannot be zero!” and stop the program.
5. Calculate attendance percentage:
attendance_percentage = (attended_classes / total_classes) × 100
6. Use conditions to decide the remark:
       If percentage ≥ 90 → Outstanding Attendance
       Else if percentage ≥ 80 → Good Attendance
       Else if percentage ≥ 70 → Attendance is Okay
       Else if percentage ≥ 50 → Low Attendance
       Else → Very Poor Attendance
7. Display:
     Attendance Percentage
     Performance Remark
8. End

FLOWCHART-:
              ┌──────────────┐
              │    START     │
              └───────┬──────┘
                      │
          ┌───────────▼───────────┐
          │ Input attended classes│
          └───────────┬───────────┘
                      │
          ┌───────────▼───────────┐
          │ Input total classes   │
          └───────────┬───────────┘
                      │
            ┌─────────▼─────────┐
            │ total_classes = 0?│
            └───────┬───────────┘
                    │YES
                    ▼
       ┌────────────────────────────┐
       │ Print "Total cannot be 0!" │
       └─────────────┬──────────────┘
                     │
                     ▼
                 ┌───────┐
                 │  END  │
                 └───────┘
                     ▲
                     │NO
          ┌──────────┴──────────┐
          │ Calculate % =       │
          │ (attended/total)*100│
          └──────────┬──────────┘
                     │
          ┌──────────▼──────────┐
          │ Check conditions    │
          │ and assign remark   │
          └──────────┬──────────┘
                     │
          ┌──────────▼──────────┐
          │ Display percentage  │
          │ and remark          │
          └──────────┬──────────┘
                     │
               ┌─────▼─────┐
               │    END    │
               └───────────┘


PYTHON CODE-:
#Attendance Performance Calculator

#This program calculates a students attendance percentage
#It then gives a performance remark

def attendance_performance(attended_classes, total_classes):
    """This function takes the number of attended classes and total classes"""

    if total_classes == 0:
        return 0, "Total classes cannot be zero!"
    
attended_classes = int(input("Enter the number of classes the student attended: "))
total_classes = int(input("Enter the total number of classes: "))


attendance_percentage = (attended_classes/total_classes)*100

if attendance_percentage >= 90:
    remark = "Outstanding Attendance!"
elif attendance_percentage >= 80:
    remark = "Good Attendance!"
elif attendance_percentage >= 70:
    remark = "Your attendance is okay!"
elif attendance_percentage >= 50:
    remark = "Low Attendance!"
else:
    remark = "Very Poor Attendance!"

print(attendance_percentage,remark)
print("ATTENDANCE PERFORMANCE CHECKER ")
print(attendance_percentage,remark)

print("\n---RESULT---")
print(f"Attendance Percentage :{attendance_percentage:.2f}%")
print(f"Performance Remark : {remark}")


OUTPUT-:
Enter the number of classes the student attended: 43
Enter the total number of classes: 50
86.0 Good Attendance!
ATTENDANCE PERFORMANCE CHECKER
86.0 Good Attendance!

---RESULT---
Attendance Percentage :86.00%
Performance Remark : Good Attendance!
