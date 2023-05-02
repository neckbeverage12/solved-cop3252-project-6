Download Link: https://assignmentchef.com/product/solved-cop3252-project-6
<br>
This assignment should give you practice with various aspects of serializing objects in Java and working with files of serialized objects. You will also get some more practice handling exceptions. Additionally, you will have a chance to get used to the basic usage of Collections in Java.

<h1>Task</h1>

Write a program to handle Student objects, including saving and loading a variable number of these objects and creating new Student objects. Your final jar file will contain the following classes

<ul>

 <li>java</li>

 <li>java</li>

</ul>

StudentHandler.java will be built entirely by you to match the sample output as well as possible.

Student.java will be edited by you. You will begin with the Student class found <a href="http://ww2.cs.fsu.edu/~thrasher/cop3252/asg/Student.java">here</a><a href="http://ww2.cs.fsu.edu/~thrasher/cop3252/asg/Student.java">.</a>

<strong>Each file should have a comment including your name at the top of the file. Each file should also have appropriate comments throughout. Make sure you indicate anywhere you change Student.java with comments</strong>

<h1>Requirements</h1>

<ol>

 <li><strong>Student Class: </strong>Most of the student class is provided for you. You will need to make changes to meet the following requirements:

  <ul>

   <li>You should be able to serialize the Student class after making changes to it</li>

   <li>All member data of the Student class should be serialized <strong>EXCEPT </strong>the double grade and any static variables (Java automatically does not attempt to serialize static member data, so you will not need to make changes to the static variables to meet this requirement, just the grade variable)</li>

   <li>You should not NEED to change anything else about the Student class, but if you do, make sure you mark it clearly with comments</li>

  </ul></li>

 <li><strong>StudentHandler Data: </strong>StudentHandler should contain one piece of data called students. This should be some collection of Student You may store this with any collection you feel is appropriate other than an array. I recommend that you use some sort of List (an ArrayList or LinkedList in particular), but feel free to use another class if you feel it is appropriate/feel more comfortable with it.</li>

 <li><strong>StudentHandler Class Methods: </strong>This class will contain your main method (discussed below) as well as the following non-static methods:

  <ul>

   <li>StudentHandler() – A single parameterless constructor, should just instantiate the member data</li>

   <li>void saveStudents(Scanner s) – This method will ask the user for a filename to save under and save the entire collection of students held in this StudentHandler as serialized objects</li>

   <li>void loadStudents(Scanner s) – This method will first clear all students out of the StudentHandler, then ask the user for a filename and load all of students stored in that file into the StudentHandler</li>

   <li>void addStudent(Scanner s) – This method will prompt the user for the various pieces of a Student object (name, grades, etc.) and create a new object and add it to the StudentHandler</li>

   <li>void printAllStudents() – This method will print all of the students, sorted by name (last name first, if those are the same, then sort by first name) as well as the count of the number of student records (you are <strong>REQUIRED </strong>to use the static totalStudents member data for this count)</li>

   <li>void clearAllStudents() – This method will clear all of the students from the collection/array</li>

  </ul></li>

 <li><strong>Main method</strong>: First, you should create a StudentHandler From there, your main method should print the menu (as seen in sample output) and ask the user for input. The user should input an integer and then you call the appropriate method (on your StudentHandler object) based on the user input. When the user inputs the integer 6, then the program should quit.</li>

 <li><strong>Error handling</strong>: You will need to handle various errors and exceptions in this project. Each of the following errors should be handled appropriately (as indicated):

  <ul>

   <li>Invalid menu input: If the user inputs invalid menu input (either a non-integer or an integer not between 1 and 6), then print an appropriate error message and go back to the beginning of your loop</li>

   <li>Invalid input in addStudent() method: If the user inputs an invalid item for any of the inputs in this method, print an appropriate error message and begin the method again (see the example output for how this should work)</li>

   <li>File exception: If there is an error reading a file for reading or writing, indicate this to the user and go back to the main menu</li>

   <li>Invalid Student File: If the user attempts to read from a file that does not contain serialized objects, this will trigger a ClassNotFoundException which you should handle by printing an error message and going back to the main menu</li>

  </ul></li>

 <li><strong>Other Requirements</strong>:

  <ul>

   <li>When saving the students, make sure you are saving each student individually rather than the entire collection (when I test, I may load your data using a different data structure in order to test your file containing serialized data).</li>

   <li>Similarly, when loading the student data, make sure you load each student individually rather than an entire collection (again, during testing, I may load a file created using a different program that contains serialized data)</li>

  </ul></li>

 <li><strong>Hints:</strong>

  <ul>

   <li>You only <strong>need </strong>the classes/methods I mention above, but if you want to add more, feel free (make them private, please)</li>

   <li>Remember to use ObjectOutputStream and ObjectInputStream for your file I/O</li>

   <li>As mentioned above, a good default collection to hold your students is an ArrayList.</li>

   <li>Pay attention to the non-serialized data when loading data from the serialized file</li>

   <li>It is especially easy to get off on your count when there are exceptions during the addStudent() method</li>

   <li>Exceptions don’t “use” the input from a Scanner, so if you are using a Scanner, make sure to include a line like NextLine() in your exceptions to process the bad input</li>

   <li>Again, remember that you are <strong>REQUIRED </strong>to use the static totalStudents member data when printing the number of students, do not simply count the elements in your collection</li>

  </ul></li>

</ol>

<h1>Sample Output</h1>

User input is underlined (there has been input before this, so there will be 3 total Students)

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>cd</u>

Invalid choice, try again.

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>2</u>

Please input a first name: <u>Joe</u>

Please input a last name: <u>Blow</u>

Please input student homework grades one at a time (negative value to finish): <u>c98</u>

Invalid input, please try inputting the student again

Please input a first name: <u>Joe</u>

Please input a last name: <u>Blow</u>

Please input student homework grades one at a time (negative value to finish): <u>98</u>

Please add another homework grade (negative value to finish): <u>77</u>

Please add another homework grade (negative value to finish): <u>-4</u>

Please input student test grades one at a time (negative value to finish): <u>75</u>

Please add another test grade (negative value to finish): <u>88</u>

Please add another test grade (negative value to finish): <u>99 </u>Please add another test grade (negative value to finish): <u>-2</u>

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>4</u>

Please input the filename to save as: <u>TheFile.txt</u>

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>1</u>

First name: Joe

Last name: Blow

Final Grade: 87.41666666666666

First name: Another

Last name: Student

Final Grade: 89.26666768391928

First name: Test

Last name: Student

Final Grade: 89.5

Printed 3 Student Records

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>3</u>

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>1</u>

Printed 0 Student Records

1: Print out all loaded students 2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>5</u>

Please input the filename to load from: <u>TheFile.txt</u>

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>1</u>

First name: Joe

Last name: Blow

Final Grade: 87.41666666666666

First name: Another

Last name: Student

Final Grade: 89.26666768391928

First name: Test

Last name: Student

Final Grade: 89.5

Printed 3 Student Records

1: Print out all loaded students

2: Add student

3: Clear students

4: Save students to file

5: Load students from file

6: Quit

Please input the number of your choice: <u>6 </u>Goodbye!