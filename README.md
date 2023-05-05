Download Link: https://assignmentchef.com/product/solved-cse240-homework-2-programming-with-c
<br>
<ol>

 <li><strong>What This Assignment Is About: </strong></li>

</ol>




<ul>

 <li>Structures</li>

 <li>Functions</li>

 <li>Arrays of Primitive Values</li>

 <li>Arrays of Structs</li>

 <li>Recursion</li>

 <li>for and if Statements</li>

 <li>Selection Sort</li>

</ul>




<strong> </strong>

<ol start="2">

 <li><strong>Use the following Guidelines</strong></li>

</ol>




<ul>

 <li>Give identifiers semantic meaning and make them easy to read (examples num_students, gross_pay, etc).</li>

 <li>Use lower case word for all identifiers (variables, functions, objects). Separate words with underscore character</li>

 <li>Use tabs or spaces to indent code within blocks (code surrounded by braces). This includes structures, functions, and code associated with ifs, switches and loops. Be consistent with the number of spaces or tabs that you use to indent.</li>

 <li>Use white space to make your program more readable.</li>

 <li>You should <strong>only submit your .c files</strong></li>

</ul>

.     homework_part_1.c

.     homework_part_2.c




<strong>For each file in your assignment, provide a heading (in comments) which includes:  </strong>

<strong> </strong>

<ul>

 <li><strong>The assignment number. </strong></li>

 <li><strong>Its author (your name). </strong></li>

 <li><strong>A description of what this program is doing.</strong></li>

</ul>




<strong> </strong>

<ol start="3">

 <li><strong>Part 1. Primitive Types, Searching, Recursion (35 points). </strong></li>

</ol>

<strong>While there could be diverse ideas to solve b and c, it is mandatory to use pointers, since the goal is for you to practice them </strong>

<strong> </strong>

<ol>

 <li>Create a file <strong>c</strong></li>

</ol>




<ol>

 <li>Create a function <strong>initialize_array</strong> that receives two parameters: an array of integers and the array size. <strong>(Use pointers to pass an array of integers as parameter)</strong> Use a for loop</li>

</ol>

and an if statement to put 5s in the odd positions of the array and 0s in the even positions. <strong>Hint: review pointers as parameters.</strong>




<ol>

 <li>Create a function <strong>print_array</strong> that receives as parameters an array of integers and the array size. <strong>(Use pointers to pass an array of integers as parameter) </strong>Use a for statements to print all the elements in the array.<strong> Hint: review pointers as parameters.</strong></li>

</ol>




<ol>

 <li>Create a function <strong>selection_sort</strong> that receives as parameters an array of integers and the array size, and order the array element in <strong><u>descending order</u></strong>. <strong>(Use pointers to pass an array of integers as parameter) </strong>Implement Selection Sort algorithm. It should be Selection Sort, not Bubble Sort, not Quick Sort, etc. If you do not remember selection sort, this link could be useful:</li>

</ol>




<a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">https://www.geeksforgeeks.org/c</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">–</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">program</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">–</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">for</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">–</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">selection</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">–</a><a href="https://www.geeksforgeeks.org/c-program-for-selection-sort/">sort/</a>




<ol>

 <li>Create a recursive function that calculate and returns the <strong>factorial</strong> of a number. The function receives the number (integer number) as parameter.</li>

</ol>

<strong> </strong>

<ol>

 <li>Copy the following main function in your class,</li>

</ol>




int main() {

int a [10] = {3, 5, 6, 8, 12, 13, 16, 17, 18, 20};       int b [6]= {18, 16, 19, 3 ,14, 6};      int c [5]= {5, 2, 4, 3, 1};

// testing initialize_array

print_array(a, 10); // print: 3, 5, 6, 8, 12, 13, 16, 17, 18, 20     selection_sort(a, 10);

print_array(a, 10); // print: 0, 5, 0, 5, 0, 5, 0, 5, 0, 5




// testing initialize_array

print_array(b, 6); // print: 18, 16, 19, 3 ,14, 6     selection_sort (b, 6);

print_array(b, 6); // print: 19, 18, 16, 14, 6, 3




// testing factorial

printf(“Factorail of 5 – %d
”, factorial (5)); //print: 120




c[0] = factorial (c[0]);     c[1] = factorial (c[2]);

print_array(c, 5); // print: 120, 24, 4, 3, 1




return 0;

}

<strong> </strong>

<h1>Grading Criteria for the part 1</h1>

01 pts: file contains header information

01 pts: adequate comment to explain every function

01 pts: consistent indentation and spacing

08 pts: selectionSort

08 pts: printArray

08 pts: initializeArray

08 pts: factorial




<ol start="4">

 <li><strong>Part 2 Structs and Arrays (65 points).</strong></li>

</ol>




In this assignment, we will be making a program that reads in students’ information and create an examination seating with a number of rows and columns specified by a user. Then it will attempt to assign each student to a seat in an examination.




Use the file <strong>homework_part_2.c</strong> (attached at the end of this document). Complete the file and include all the following requested code in the file homework_part_2.c

<strong> </strong>

<strong><u>Step 1.</u></strong><strong>  </strong>




First, you need to create a structure <strong>student</strong><strong>.</strong> It should contain two variables, last_name (char [30]) and first_name (char [30]). In addition, the following functions should be defined.




<table width="632">

 <tbody>

  <tr>

   <td width="264"><strong>Function </strong></td>

   <td width="368"><strong>Description</strong></td>

  </tr>

  <tr>

   <td width="264">void student_init_default  (struct student *p)</td>

   <td width="368">Assign the default string ” ### ” to both variables, last_name and first_name. </td>

  </tr>

  <tr>

   <td width="264">void student_init(struct student *p, char *info)</td>

   <td width="368">Use the <strong>strtok function</strong> to extract first name and last name from the variable student, then assign them to each instance variable of the <strong>student</strong> structure. An example of the input string is:David/Johnson </td>

  </tr>

  <tr>

   <td width="264">void student_to_string (struct student *p)</td>

   <td width="368">It prints the initial character of the first name, a period, the initial character of the last name, and a period. An example of such string for the student David Johnson is:<em>D.J.  </em> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong><u>Step 2.</u></strong>




You will be creating a structure called <strong>examination_seating</strong> in the same code file. The structure examination_seating will contain a 2-dimensional array called “seating” of <strong>student</strong> type. <strong>(Note: student is a structure you created above). </strong>You will also need to create variables to check rows and columns for the seating (If your code does not contain any of the following functions, points will be deducted.) Define the following functions:







<table width="633">

 <tbody>

  <tr>

   <td width="255"><strong>Function</strong></td>

   <td width="378"><strong>Description</strong></td>

  </tr>

  <tr>

   <td width="255"> void examination_seating_init  (int rowNum, int columnNum,  struct examination_seating *t )</td>

   <td width="378">It instantiates a two-dimensional array of the size “rowNum” by “columnNum” specified by the parameters inside the struct <strong>t</strong>. Then it initializes each student element of this array using the <strong>student_init_default </strong>function. So, each student will have default values for its instance variables. </td>

  </tr>

  <tr>

   <td width="255">int assign_student_at  (int row, int col,struct examination_seating *t,  struct student* p)</td>

   <td width="378">The function attempts to assign the “p” to the seat at “row” and “col” (specified by the parameters of this function). If the seat has a default student, i.e., a student with the last name “###” and the first name “###”, then we can assign the new student “p” to that seat and the method returns true. Otherwise, this seat is considered to be taken by someone else, the method does not assign the student and return <strong>0</strong> (false). </td>

  </tr>

  <tr>

   <td width="255">int check_boundaries  (int row, int col,struct examination_seating *t)</td>

   <td width="378">The function checks if the parameters row and col are valid. If at least one of the parameters “row” or “col” is less than “0” or larger than the last index of the array (note that the number of rows and columns can be different), then it return 0 (false). Otherwise it returns 1 (true). </td>

  </tr>

  <tr>

   <td width="255">void examination_seating_to_string (struct examination_seating *t )</td>

   <td width="378">It prints information of the “seating”. It should show the list of students assigned to the seating using the <strong>student_to_string</strong> function (it shows initials of each student) and the following format: The current seating——————–  D.J. #.#. E.T.#.#. #.#. S.W.T.C. A.T. #.#. Please see the sample output listed below. </td>

  </tr>

 </tbody>

</table>




After compiling the <strong>homework_part_2.c</strong> file, you need to execute it.













<strong>            </strong>

<h1>Sample Output: (the inputs entered by a user are shown in bold)</h1>




Make sure that your program works at least with this scenario.




Please enter a number of rows for a examination seating.

<strong>3</strong>

Please enter a number of columns for a examination seating.

<strong>3</strong>

Please enter a student information or enter “Q” to quit.

<strong>Mickey/Mouse </strong>

A student information is read.

Mickey/Mouse

Please enter a row number where the student wants to sit.

<strong>1</strong>

Please enter a column number where the student wants to sit.

<strong>2 </strong>

The seat at row 1 and column 2 is assigned to the student M.M.




The current seating

——————–

#.#. #.#. #.#. 
#.#. #.#. M.M.

#.#. #.#. #.#.




<table width="404">

 <tbody>

  <tr>

   <td colspan="2" width="404">Please enter a student information or enter “Q” to quit.</td>

  </tr>

  <tr>

   <td width="72"><strong>Daisy/Duck</strong></td>

   <td width="331"><strong> </strong></td>

  </tr>

 </tbody>

</table>




A student information is read.

Daisy/Duck

Please enter a row number where the student wants to sit.

<strong>2</strong>

Please enter a column number where the student wants to sit.  <strong>0 </strong>




The seat at row 2 and column 0 is assigned to the student D.D.




The current seating

——————–

#.#. #.#. #.#.

#.#. #.#. M.M.

D.D. #.#. #.#.




<table width="404">

 <tbody>

  <tr>

   <td colspan="2" width="404">Please enter a student information or enter “Q” to quit.</td>

  </tr>

  <tr>

   <td width="101"><strong>Clarabelle/Cow</strong></td>

   <td width="302"><strong> </strong></td>

  </tr>

 </tbody>

</table>




<table width="216">

 <tbody>

  <tr>

   <td colspan="2" width="216">A student information is read.</td>

  </tr>

  <tr>

   <td width="101">Clarabelle/Cow</td>

   <td width="115"> </td>

  </tr>

 </tbody>

</table>




Please enter a row number where the student wants to sit.

<strong>2 </strong>

Please enter a column number where the student wants to sit.  <strong>1 </strong>




The seat at row 2 and column 1 is assigned to the student C.C.




The current seating

——————–

#.#. #.#. #.#. 
#.#. #.#. M.M.

D.D. C.C. #.#.




Please enter a student information or enter “Q” to quit.

<strong>Max/Goof </strong>

A student information is read.

Max/Goof

Please enter a row number where the student wants to sit.

<strong>0</strong>

Please enter a column number where the student wants to sit.  <strong>0 </strong>




The seat at row 0 and column 0 is assigned to the student M.G.




The current seating

——————–  M.G. #.#. #.#.

#.#. #.#. M.M.

D.D. C.C. #.#.




Please enter a student information or enter “Q” to quit.

<strong>Horace/Horsecollar </strong>

A student information is read.

Horace/Horsecollar




Please enter a row number where the student wants to sit.

<strong>5</strong>

Please enter a column number where the student wants to sit.

<strong>1 </strong> row or column number is not valid.

A student Horace Horsecollar is not assigned a seat.

<table width="404">

 <tbody>

  <tr>

   <td colspan="3" width="404">Please enter a student information or enter “Q” to quit.</td>

  </tr>

  <tr>

   <td width="123"><strong>Sylvester/Shyster</strong></td>

   <td colspan="2" width="281"><strong> </strong></td>

  </tr>

  <tr>

   <td colspan="2" width="216">A student information is read.</td>

   <td rowspan="2" width="187"> </td>

  </tr>

  <tr>

   <td width="123">Sylvester/Shyster</td>

   <td width="94"> </td>

  </tr>

 </tbody>

</table>




Please enter a row number where the student wants to sit.

<strong>2 </strong>

Please enter a column number where the student wants to sit.

<strong>0 </strong>

The seat at row 2 and column 0 is taken.

Please enter a student information or enter “Q” to quit.

<strong>Snow/White </strong>




A student information is read.

Snow/White

Please enter a row number where the student wants to sit. 
<strong>-1</strong>




Please enter a column number where the student wants to sit.  <strong>0 </strong>

row or column number is not valid.

A student Snow White is not assigned a seat.

Please enter a student information or enter “Q” to quit.

<strong>Jiminy/Criket </strong>




<table width="417">

 <tbody>

  <tr>

   <td colspan="2" width="222">A student information is read.</td>

   <td rowspan="2" width="194"> </td>

  </tr>

  <tr>

   <td width="100">Jiminy/Criket</td>

   <td width="122"> </td>

  </tr>

  <tr>

   <td colspan="3" width="417">Please enter a row number where the student wants to sit.</td>

  </tr>

  <tr>

   <td width="106"></td>

   <td width="120"></td>

   <td width="191"></td>

  </tr>

 </tbody>

</table>




The seat at row 0 and column 2 is assigned to the student J.C.










<h1>Grading Criteria for the part 2</h1>




05 pts: Every file contains header information

05 pts: adequate comment to explain every function

05 pts: consistent indentation and spacing

05 pts: it compiles

10 pts: The functions student_init are correct

05 pts: The function student_to_string method is correct

10 pts: The function examination_seating_init is correct

10 pts: The function assign_student_at (int, int, p) method is correct

05 pts: The function check_boundaries(int, int) method is correct

05 pts: The function examination_seating_to_string method is correct














































































































































#include &lt;stdio.h&gt; struct student {  char last_name[30] ;  char first_name[30];

};

struct examination_seating {  struct student **seating;

};

void student_init_default (struct student *p ) {} void student_init (struct student *p, char *info) {} void student_to_string (struct student *p ) {}

void examination_seating_init (int rowNum, int columnNum, struct examination_seating *t ) {} int assign_student_at (int row, int col, struct examination_seating *t, struct student* p) {} int check_boundaries (int row, int col, struct examination_seating *t) {} void examination_seating_to_string (struct examination_seating *t ) {}

void main() {

struct examination_seating examination_seating;    struct student temp_student;




int row, col, rowNum, columnNum;    char student_info[30];

// Ask a user to enter a number of rows for a examination seating       printf (“Please enter a number of rows for a examination seating.”);    scanf (“%d”, &amp;rowNum);




// Ask a user to enter a number of columns for a examination seating      printf (“Please enter a number of columns for a examination seating.”);      scanf (“%d”, &amp;columnNum);




// examination_seating

examination_seating_init(rowNum, columnNum, &amp;examination_seating);




printf(“Please enter a student information or enter ”Q” to quit.”);




/*** reading a student’s information ***/    scanf (“%s”, student_info);




/* we will read line by line **/    while (1 /* change this condition*/ ){      printf (“
A student information is read.”);

// printing information.      printf (“%s”, student_info);

// student

student_init (&amp;temp_student, student_info);

// Ask a user to decide where to seat a student by asking

// for row and column of a seat




printf (“Please enter a row number where the student wants to sit.”);      scanf(“%d”, &amp;row);




printf(“Please enter a column number where the student wants to sit.”);      scanf(“%d”, &amp;col);

// Checking if the row number and column number are valid       // (exist in the examination that we created.)      if (check_boundaries(row, col, &amp;examination_seating) == 0) {        printf(“
row or column number is not valid.”);

printf(“A student %s %s is not assigned a seat.”, temp_student.first_name, temp_student.last_name);

} else {

// Assigning a seat for a student

if (assign_student_at(row, col, &amp;examination_seating, &amp;temp_student) == 1){          printf(“
The seat at row %d and column %d is assigned to the student”,row, col);         student_to_string(&amp;temp_student);

examination_seating_to_string(&amp;examination_seating);

} else {

printf(“
The seat at row %d and column %d is taken.”, row, col);

}

}

// Read the next studentInfo

printf (“Please enter a student information or enter ”Q” to quit.”);

/*** reading a student’s information ***/     scanf(“%s”, student_info);

}




}