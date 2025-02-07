# Machine Learning Specialization by Deep Learning.AI & Stanford University

# Usage:
1. clone repository with `git clone https://github.com/08Miguel24/machine-learning-specialization-hw.git`
2. navigate to directory with `readme.md` and `requirements.txt` file
3. run command; `conda create -n <name of env e.g. machine-learning-specialization-hw> python=3.10.9`. Note that 3.10.9 must be the python version otherwise packages to be installed would not be compatible with a different python version
4. once environment is created activate it by running command `conda activate`
5. then run `conda activate machine-learning-specialization-hw`
6. check if pip is installed by running `conda list -e` and checking list
7. if it is there then move to step 8, if not then install `pip` by typing `conda install pip`
8. if `pip` exists or install is done run `pip install -r requirements.txt` in the directory you are currently in

# Side Notes:
1. DO record the assignment token provided on the exercise page, 
you will need it to submit your solutions. 

when submitting enter exercise number and then enter email

2. you do not need to include the ".m" portion of the script file name, so, run the Exercise 1 script by typing just "ex1" at the command line.

3. You also do not need to include parenthesis () when using the submit script. Just type "submit". 

4. The submit grader uses a different test case than what is in the PDF file. 
SimilaR TO LEETCODE, Your code must work correctly with any size of data  set.

5. So, every line of code should end with a semicolon.

6. If your code runs but gives the wrong answers, you can insert a "keyboard" command in your script
This will cause the program to exit to the debugger, so you can inspect all your variables from the command line

7. It is always a good idea to test your functions using the unit tests before submitting to the grader.

8. If you run the submit script and get a message that your identity can't be 
verified, be sure that you have logged-in using your Coursera account email 
and your Programming Assignment submission password

9.  If you get the message "submit undefined", first check that 
you are in the working directory where you extracted the files 
from the ZIP archive. Use "cd" to get there if necessary. 

10.  If the "submit undefined" error persists, or any other "function undefined" 
messages appear, try using the "addpath(pwd)" command to add your present 
working directory (pwd) to the Octave execution path. 

11. If the submit script/function crashes with an error message, please see 
the  thread "Mentor tips for submitting your work" under "All Course  
Discussions".





summary of writing the functions
note always be in directory of exercise folder in matlab drive
1. look for * beside the filenames because this will need to be completed
2. open it
3. exn.mlx will contain the code sections which call the functions inside those files
with those filenames that you will have to complete, thus testing your written function
4. those sections can be run by the click path live editor > run section
5. once a section or the whole exercise is done type the submit command in the command line
6. to run a .m file type the filename without the .m extension in the command window if in octave


% this is a comment
disp(sprintf("<some string> %0.2f %0.6this means 2 decimal plaecs")
pi is a constant 3.14

when you don;'t want to print a line through the console put a semi colopn at the end of that line

matrices
A = [1 2; 3 4; 5 6] is equivalent to [[1, 2], [3, 4], [5, 6]]
v = [1 2 3] row vector
v = [1; 2; 3] column vector
v = [<start value>:<increment value>:<end value, inclusive>] or [<start value>:<end value>]
v = <start value>:<end value>
v = [1:0.1:2] % this outputs a vector
v = ones(<dimensionionality e.g. <number of rows>, <number of columns>>)
v = zeroes(<dimensionality e.g. < number of rows>, <number of columns>>)
v = rand(<dimensionality e.g. < number of rows>, <number of columns>>)
v = randn(<dimensionality e.g. < number of rows>, <number of columns>>)
v = eye(<dimensionality of identity matrix e .g. 5  produces 5x5 identity matrix>	



data indexing and manipulation
TO NOTE: INDEXING IN MATLAB DOES NOT START FROM 0 to N-1 but from 1 to N
<vector>(<start index value>:<end index value>) % returns a slice of the vector based on its start and end index
e.g. 1:10 gets only the elements with index 1 to 10 of a vector 

<matrix>(<row index>, <column index>) 
<matrix>(<row index>,:) - fetches every column element of a certain row index just like <list>[:] in python
<matrix>([<row index 1>, <row index a>, ..., <row index z>], :) - like how we can use an array of number that
denote the indeces of the dataframe to access, to access a dataframe in pandas in matlab we can also do this

<matrix> = [<matrix>, [100; 101; 102]]; % appends another column vector to the right of the matrix
<matrix C> = [<matrix A> <matrix B>]; % concatenates matrix B to the right of matrix A or along the x axis
or <matrix C> = [<matrix A>, <matrix B>]; 

<matrix C> = [<matrix A>; <matrix B>]; % concatenates matrix B to the bottom of matrix A or along the Y axis
<matrix C>'; % is the transpose of a matrix

<matrix or vector> * <scalar> = matrix or vecotr
<matrix or vector> .* <matrix or vector> = <matrix of the same dimensionality>; % this is because element wise multiplication just uses an element of matrix A and multiplies it to the element with teh same index in matrix B

<scalar> ./ <matrix or vector = <matrix or vecotr of same dimensinality>; % this is element wise division of scalar precedes the matrix first in the operation
note that when using a scalar in an operation that precedes a vector or matrix you should
always use an element wise operation such as .*, ./, .^, excluding +, - operations

log(<matrix or vector>) = <natural log of the matrix or vector by getting natural log of each value in matrix or vector>
exp(<natrix ir vector) = <raise the the matrix or vector values to the natural number e>
abs(<matrix or vector) = <matrix or vector of same dimensionality> % takes the absolute value of each value in each matrix or vector

<vector> * <vector>' = <scalar> % this operation produces the sum of squares of each value in the vector or matrix
<vector matrix> .* <vector or matrix> = <vector or matrix of same dimensionality> % this is usually good when squaring the elements of vector or matrix


sz = size(<matrix or vector>, <if value is 1 then return the number of rows of the matrix or vector if 2 then columns>) % sz is actually also a vector of size 
(1, 2) the two columns being the representations of the number of 
rows and number of columsn respectively of the matrix or number of 
elements if a vector 

length(<matrix or vector>) % returns the largest dimension of the matrix or vector


raising eulers number to a vector or matrix of values cannot be done in matlab so how to implement sigmoid?




loading data

load <filename>.dat or load('<filename>.dat>')
save <filename>.mat <vector or matrix variable> - saves the matrix or vector of certain values to a file
save <filename>.txt <vector or matrix variable> - saves the matrix or vector of certain 
values to a text file that is easily readable and understandable


visualization
hist(<matrix or vector>, <number of bars in the histogram>)


help
help <name of function reveals how the function works and the parameters it has


pwd - means parent working directory to check the directory currently workin in
ls - 
who - lists out the variables in the current scope
whos - lsits out the variables in the current scope as well as its details 
e.g. attr, name, size, bytes, class or data type
clear <variable> -
clear - clears all variables

