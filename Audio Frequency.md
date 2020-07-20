## Project 2. - Audio Frequency
This project is designed to help you to wrap up the MATLAB coding skills of Day 1
Audio signals are usually composed of many different frequencies. 
For example, in music, the note 'middle C' has a frequency of 261.6 Hz, 
and most music consists of several notes (or frequencies) being played at the same time.
Typically, the frequencies that make up a signal are different enough that 
they do not interfere substantially with each other.
However, when a signal contains two frequencies that are close together, 
they can cause the signal to appear to have a 'beat' - a pulsing pattern in the amplitude.
In this project, you will create a signal that contains this beat phenomenon 
and then analyze the signal's frequency content. fs will represent the sampling frequency of the audio signal.

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
<img width="1017" alt="Screen Shot 2020-07-19 at 9 45 07 AM" src="https://user-images.githubusercontent.com/46945617/87876631-6a65cf80-c9a7-11ea-8384-2f631e307129.png">

#### Use the data cursor in the output pane to see the frequency locations.

<img width="382" alt="Screen Shot 2020-07-19 at 9 45 35 AM" src="https://user-images.githubusercontent.com/46945617/87876630-69cd3900-c9a7-11ea-8105-d3d8db255081.png">
