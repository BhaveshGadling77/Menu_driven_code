#### Student Grades Query System
#### Overview 

This C program processes student grades from three CSV files (subjects.csv, grades.csv, and marks.csv) and supports various queries related to grades, CGPA, SGPA, toppers, and statistics.
Input Files
subjects.csv

Format:

subject-name,no-of-credits,semester

Example:

os,4,3
dsa,3,2

grades.csv

Each row specifies grade boundaries for a subject.

Format:

ub4,ub5,ub6,ub7,ub8,ub9,ub10

Example:

40,50,60,70,80,90,95

marks.csv

Each row contains student MIS ID followed by marks in subjects.

Format:

MIS_ID,sub1_marks,sub2_marks,...

Example:

11122312,85,78,92
11010101,45,60,30

Commands

    grade <MIS> <subject> – Get a student's grade.
    grade all – Display grades of all students.
    cgpa <MIS> – Compute CGPA of a student.
    sgpa <MIS> <sem> – Compute SGPA for a semester.
    failed <MIS> – List subjects failed by a student.
    topsem <sem> – Show top students per subject in a semester.
    topsub <subject> – Show the topper in a subject.
    topnsub <subject> <n> – List top n students in a subject.
    stdev <subject> – Compute standard deviation of marks.
    exit – Quit the program.

Running the Program

Ensure all CSV files are in the working directory, then compile and run:

gcc main.c -o grades
./grades

Enter commands at the > prompt.
Example Queries

> grade 11122312 os
AA
> cgpa 11122312
9.00
> failed 11010101
dsa
> topnsub os 2
112312321, 92
11122312, 85
> exit
