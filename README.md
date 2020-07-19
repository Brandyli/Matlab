# Matlab
## Project 1. Electricity Usage

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
## Project 2. - Audio Frequency
% This project is designed to help you to wrap up the MATLAB coding skills of Day 1

% Audio signals are usually composed of many different frequencies. 
% For example, in music, the note 'middle C' has a frequency of 261.6 Hz, 
% and most music consists of several notes (or frequencies) being played at the same time.
% Typically, the frequencies that make up a signal are different enough that 
% they do not interfere substantially with each other.
% However, when a signal contains two frequencies that are close together, 
% they can cause the signal to appear to have a 'beat' - a pulsing pattern in the amplitude.
% In this project, you will create a signal that contains this beat phenomenon 
% and then analyze the signal's frequency content.

% fs will represent the sampling frequency of the audio signal.

```
Task 1
load Cchord.mat
n = numel(y)
t=(0:1:n-1)

Task 2
t=(t/fs)
plot(t,y)


Task 3
yfft=abs(fft(y))

Task 4
f=(0:1:n-1)


Task 5
f=f*fs/n
plot(f,yfft)
xlim([0,1000])
```
<img width="382" alt="Screen Shot 2020-07-19 at 9 45 35 AM" src="https://user-images.githubusercontent.com/46945617/87876630-69cd3900-c9a7-11ea-8105-d3d8db255081.png">
Use the data cursor in the output pane to see the frequency locations.
<img width="1017" alt="Screen Shot 2020-07-19 at 9 45 07 AM" src="https://user-images.githubusercontent.com/46945617/87876631-6a65cf80-c9a7-11ea-8384-2f631e307129.png"> 
