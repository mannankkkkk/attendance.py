# attendance_tracker.py

# Initialize an empty dictionary to store attendance records
attendance_records = {}

def mark_attendance(student_name):
    """
    Mark attendance for a student.
    """
    if student_name in attendance_records:
        print(f"{student_name} has already been marked present.")
    else:
        attendance_records[student_name] = True
        print(f"{student_name} has been marked present.")

def main():
    while True:
        print("\nAttendance Tracker")
        print("1. Mark Attendance")
        print("2. View Attendance Records")
        print("3. Exit")
        
        choice = input("Enter your choice: ")
        
        if choice == '1':
            student_name = input("Enter student name: ")
            mark_attendance(student_name)
        elif choice == '2':
            print("\nAttendance Records:")
            for student, attendance in attendance_records.items():
                print(f"{student}: {'Present' if attendance else 'Absent'}")
        elif choice == '3':
            print("Exiting Attendance Tracker.")
            break
        else:
            print("Invalid choice. Please choose again.")

if __name__ == "__main__":
    main()
