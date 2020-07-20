## Project 1. Electricity Usage
In this project, you will understand

Vectors and Matrices
Create MATLAB variables that contain multiple elements.

Indexing into and Modifying Arrays
Use indexing to extract and modify rows, columns, and elements of MATLAB arrays.

Array Calculations
Perform calculations on entire arrays at once.

Calling Functions
Call functions to obtain multiple outputs.

Plotting Data
Visualize variables using MATLAB's plotting functions.
Logical Arrays
Use logical expressions to help you to extract elements of interest from MATLAB arrays.

```
Task 1
load electricity.mat
usage


Task 2
% One of the elements in the usage variable has a value of NaN. 
% Replace this value with the value 2.74.

usage(2,3)=2.74 % replace NaN

Task 3
% The residential data is stored in the first column. 
% Create a variable res that contains the first column of usage.
res=usage(:,1)

Task 4
% The commercial data and industrial data are stored 
% in the second and third column, respectively. 
% Create variables comm and ind that 
% contain the second and third columns of usage.
comm=usage(:,2)
ind=usage(:,3)


Task 5
% The usage data was collected annually 
% between the years 1991 to 2013. 
% The yrs variable you create will help you to 
% plot the data over a meaningful range.
yrs=[1991:2013]

Task 6
% Create a plot with all three columns. 
% Use yrs as the x-data. 
% Use this order and these plot specifications:
% res: blue (b) dashed line (--)
% comm: black (k) dotted line (:)
% ind: magenta (m) dash-dot line (-.)
plot(yrs,res,"b--")
hold on
plot(yrs,comm,"k:")
hold on
plot(yrs,ind,"m-.")

Task 7
% Add the title "July Electricity Usage" to the existing plot.
% Create a legend with the values "res", "comm", and "ind".
title("July Electricity Usage")
legend("res", "comm","ind")
```
<img width="996" alt="Screen Shot 2020-07-19 at 10 03 44 AM" src="https://user-images.githubusercontent.com/46945617/87876642-92553300-c9a7-11ea-9c16-c161a6d3289a.png">
<img width="977" alt="Screen Shot 2020-07-19 at 10 04 04 AM" src="https://user-images.githubusercontent.com/46945617/87876641-91bc9c80-c9a7-11ea-859a-4a63205e2ca9.png">
