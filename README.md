# School Management System

This is a simple School Management System implemented in Python. The system allows for the management of classrooms, students, teachers, and subjects, along with conducting semester final exams for different classes.

## Modules

- **school.py**: Contains the `School` class.
- **person.py**: Contains the `Person`, `Student`, and `Teacher` classes.
- **subject.py**: Contains the `Subject` class.
- **classroom.py**: Contains the `ClassRoom` class.

## Classes and Their Responsibilities

### School
- **Attributes**: 
  - `name`: Name of the school.
  - `address`: Address of the school.
  - `teachers`: Dictionary mapping subjects to teacher objects.
  - `classrooms`: Dictionary mapping classroom names to classroom objects.
- **Methods**:
  - `add_classroom(classroom)`: Adds a classroom to the school.
  - `add_teacher(subject, teacher)`: Adds a teacher for a specific subject.
  - `student_admission(student)`: Admits a student to the appropriate classroom.
  - `calculate_grade(marks)`: Static method to calculate grade from marks.
  - `grade_to_value(grade)`: Static method to convert grade to grade point value.
  - `value_to_grade(value)`: Static method to convert grade point value to grade.
  - `__repr__()`: Returns a detailed string representation of the school, including classrooms, students, subjects, and student results.

### ClassRoom
- **Attributes**:
  - `name`: Name of the classroom.
  - `students`: List of students in the classroom.
  - `subjects`: List of subjects taught in the classroom.
- **Methods**:
  - `add_student(student)`: Adds a student to the classroom and assigns a roll number.
  - `add_subject(subject)`: Adds a subject to the classroom.
  - `take_semester_final_exam()`: Conducts semester final exams for all subjects in the classroom and calculates final grades for all students.
  - `__str__()`: Returns a string representation of the classroom and its subjects.

### Person
- **Attributes**:
  - `name`: Name of the person.

### Teacher (inherits from Person)
- **Attributes**:
  - `name`: Name of the teacher.
- **Methods**:
  - `evaluate_exam()`: Randomly generates and returns a mark between 50 and 100.
  - `__str__()`: Returns a string representation of the teacher.

### Student (inherits from Person)
- **Attributes**:
  - `name`: Name of the student.
  - `classroom`: Classroom of the student.
  - `id`: Roll number of the student.
  - `marks`: Dictionary of subject marks.
  - `subject_grade`: Dictionary of subject grades.
  - `grade`: Final grade of the student.
- **Methods**:
  - `calculate_final_grade()`: Calculates the final grade of the student based on exam results.
  - `__str__()`: Returns a string representation of the student.
  - `id`: Property to get and set the student's roll number.

### Subject
- **Attributes**:
  - `name`: Name of the subject.
  - `teacher`: Teacher of the subject.
  - `max_marks`: Maximum marks for the subject (default is 100).
  - `pass_marks`: Passing marks for the subject (default is 33).
- **Methods**:
  - `exam(students)`: Conducts exams for the given list of students by assigning marks and calculating grades.
  - `__str__()`: Returns a string representation of the subject and its teacher.

## Usage

Markup :  [project Link](https://docs.google.com/document/d/1P8fTx06L_RwnEpOAgcxd-SiMBUvb4BlZKUs1UtA9LU4/edit "School Management System")