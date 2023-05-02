Download Link: https://assignmentchef.com/product/solved-comp1410-assignment-5-dynamic-linked-lists-and-file-manipulation
<br>
<strong><u>Dynamic Linked Lists and File Manipulation</u></strong>

Through this assignment, you are going to be maintaining a file of all students and their registered courses to learn the concepts of structures, pointers to structures, dynamic memory allocation and file manipulation. For this, a structure called “studentInfo” with the following member elements should be defined:

<ul>

 <li><strong>StudentID – 9 char long </strong></li>

 <li><strong>First Name – 20 char long </strong></li>

 <li><strong>Last Name – 25 char long </strong></li>

 <li><strong>Number of Courses Attending – integer </strong></li>

 <li><strong>Array of CourseInfo – a 10 element array of courseInfo elements </strong></li>

 <li><strong>next – Pointer to the next student structure in the list</strong></li>

</ul>

where the CourseInfo structure has been defined as follow:

<strong>struct CourseInfo{     int courseID;     char courseName[30]; </strong>

<strong>}; </strong>




<strong>Your task is to: </strong>

Write a complete, well documented C program that will be able to:

<ol>

 <li>Add a new student</li>

 <li>Delete a student and all information related to that student</li>

 <li>Search for a student and their information</li>

 <li>Display a list of current students</li>

 <li>Save student information to file</li>

 <li>Load student information from file</li>

</ol>




<strong>Assignment Description:  </strong>

You are provided with a data file called “studentList.txt” that has the data for a number of students. You are required to read this data from the input file into <strong>a sorted linked list</strong> data structure. The linked list must be sorted based on the StudentID. The sample input file will end with a line that has three stars. An example of an input file with two fictional students is:

<table width="0">

 <tbody>

  <tr>

   <td width="193">studentList.txt</td>

  </tr>

  <tr>

   <td width="193">111111111LisaPorter3ENEE 114CMSC 412ENME 515333333333AlexSimpson1CMSC 412***</td>

  </tr>

 </tbody>

</table>




For each student, the data file is formatted line by line in the following manner: <strong>&lt;student ID&gt; </strong>

<strong>&lt;first name&gt; </strong>

<strong>&lt;last name&gt; </strong>

<strong>&lt;number of courses they are taking&gt; </strong>

<strong>&lt;course name&gt; &lt;course id&gt;  </strong>




After loading the student list, your program should be able to interactively ask the user for input. Your interactive menu should have the following inputs:

<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong><strong> </strong></li>

</ol>

<strong>Hints</strong><strong>:  </strong>

<strong> </strong>

<ul>

 <li>The following points are to be considered:

  <ol>

   <li>Student ID should be unique and 9 characters of numbers (such as 123456789, 103449977)</li>

   <li>First name and Last Name should be started with capital letters (upper case).</li>

   <li>Student information should be sorted based on the student IDs both in the linked list and in the input/output file.</li>

  </ol></li>

 <li>Your program should implement at least the following functions:

  <ol>

   <li><strong>addStudent ()</strong> : To add a new student and his/her registered courses.

    <ul>

     <li>Make sure the first letter of the first and last names is upper case (capital letter).</li>

     <li>The student ID should be unique; you cannot have two students with the same StudentID. So, before adding a student, search for the studentID to be sure that you have not had it previously entered.</li>

     <li>If the linked list is empty, the new student is the head of the list. If not, search through the linked list to find the appropriate spot within the sorted linked list.</li>

    </ul></li>

   <li><strong>deleteStudent(): </strong>To delete a student information using its StudentID.

    <ul>

     <li>Search the linked list for a student matching the studentID passed in. If it is found, delete it from the linked list.</li>

     <li>Note that the linked list is sorted based on studentID!</li>

    </ul></li>

   <li><strong>searchStudentID(): </strong>To search for a student using studentID

    <ul>

     <li>You do not have to search all the linked list as it is sorted based on studendIDs. – This function can be called from addStudent() and deleteStudent() functions.</li>

    </ul></li>

   <li><strong>searchStudentlName(): </strong>To search for a student using his/her last name and display the related information if the student exists.

    <ul>

     <li>You have to search all the linked list as it is not sorted based on last names</li>

     <li>Before starting the search, make sure the name supplied by the user has a capital letter for the first letter.</li>

    </ul></li>

   <li><strong>displayStudentInfo(): </strong>To display the current student information that exists in the linked list</li>

   <li><strong>saveStudentInfo(): </strong>To save student information from the sorted linked list to a file (inputStudents.txt)</li>

   <li><strong>loadStudentinfo(): </strong>To read all the student information from an input file (studentList.txt)

    <ul>

     <li>This function should be called at the beginning of you program to load all previous student information saved in the input file</li>

     <li>Student information should be formatted and stored in a sorted linked list.</li>

    </ul></li>

   <li><strong>exit(): </strong>To save student information in a file (inputStudents.txt) and exit from the program</li>

  </ol></li>

</ul>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Sample Run </strong>

A sample run of the program, with its interactive menu is shown below.




<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong></li>

</ol>

&gt; 1

Adding new student:

Student ID : 222222222

First name : john

Last name : Rezaei

Number of courses: 2

Course ID: 412

Course Name: CMSC

Course ID: 123

Course Name: MATH




<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong>&gt; 4  Student 1:</li>

</ol>

111111111

Lisa

Porter

3

ENEE 114

CMSC 412

ENME 515




Student 2:

222222222

John

Rezaei

2

CMSC 412

MATH 123




Student 3:

333333333

Alex

Simpson

1

CMSC 412

<strong> </strong>

<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong></li>

</ol>

&gt; 3

What is the last name of student? porter

111111111

Lisa

Porter

3

ENEE 114

CMSC 412

ENME 515




<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong></li>

</ol>

&gt; 2

Student ID: 111111111 Student information deleted.




<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong>&gt; 4  Student 1:</li>

</ol>

222222222

John

Rezaei

2

CMSC 412

MATH 123




Student 2:

333333333

Alex

Simpson

1

CMSC 412




<ol>

 <li><strong>Add new student </strong></li>

 <li><strong>Delete a student </strong></li>

 <li><strong>Search for a student </strong></li>

 <li><strong>Display current students </strong></li>

 <li><strong>Save student information to file </strong></li>

 <li><strong>Exit </strong></li>

</ol>

&gt; 6

Save student information to file before leaving? y  Student List saved successfully.  Bye!


