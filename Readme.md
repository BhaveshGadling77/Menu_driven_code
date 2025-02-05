<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Grades Query System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1, h2 {
            color: #333;
        }
        code {
            background: #eee;
            padding: 3px 5px;
            border-radius: 3px;
        }
        pre {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
    </style>
</head>
<body>

    <h1>Student Grades Query System</h1>

    <h2>Overview</h2>
    <p>This C program processes student grades from three CSV files (<code>subjects.csv</code>, <code>grades.csv</code>, and <code>marks.csv</code>) and supports various queries related to grades, CGPA, SGPA, toppers, and statistics.</p>

    <h2>Input Files</h2>

    <h3>subjects.csv</h3>
    <p><strong>Format:</strong></p>
    <pre>subject-name,no-of-credits,semester</pre>
    <p><strong>Example:</strong></p>
    <pre>os,4,3
dsa,3,2</pre>

    <h3>grades.csv</h3>
    <p>Each row specifies grade boundaries for a subject.</p>
    <p><strong>Format:</strong></p>
    <pre>ub4,ub5,ub6,ub7,ub8,ub9,ub10</pre>
    <p><strong>Example:</strong></p>
    <pre>40,50,60,70,80,90,95</pre>

    <h3>marks.csv</h3>
    <p>Each row contains student MIS ID followed by marks in subjects.</p>
    <p><strong>Format:</strong></p>
    <pre>MIS_ID,sub1_marks,sub2_marks,...</pre>
    <p><strong>Example:</strong></p>
    <pre>11122312,85,78,92
11010101,45,60,30</pre>

    <h2>Commands</h2>
    <ul>
        <li><code>grade &lt;MIS&gt; &lt;subject&gt;</code> – Get a student's grade.</li>
        <li><code>grade all</code> – Display grades of all students.</li>
        <li><code>cgpa &lt;MIS&gt;</code> – Compute CGPA of a student.</li>
        <li><code>sgpa &lt;MIS&gt; &lt;sem&gt;</code> – Compute SGPA for a semester.</li>
        <li><code>failed &lt;MIS&gt;</code> – List subjects failed by a student.</li>
        <li><code>topsem &lt;sem&gt;</code> – Show top students per subject in a semester.</li>
        <li><code>topsub &lt;subject&gt;</code> – Show the topper in a subject.</li>
        <li><code>topnsub &lt;subject&gt; &lt;n&gt;</code> – List top <code>n</code> students in a subject.</li>
        <li><code>stdev &lt;subject&gt;</code> – Compute standard deviation of marks.</li>
        <li><code>exit</code> – Quit the program.</li>
    </ul>

    <h2>Running the Program</h2>
    <p>Ensure all CSV files are in the working directory, then compile and run:</p>
    <pre>gcc main.c -o grades
./grades</pre>
    <p>Enter commands at the <code>&gt;</code> prompt.</p>

    <h2>Example Queries</h2>
    <pre>&gt; grade 11122312 os
AA
&gt; cgpa 11122312
9.00
&gt; failed 11010101
dsa
&gt; topnsub os 2
112312321, 92
11122312, 85
&gt; exit</pre>

</body>
</html>
