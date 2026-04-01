# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MATLAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001;

%Low Pass Filter Coefficient
n=0:1:N-1; 
hd=sin(wc*(n-alpha+eps))./(pi*(n-alpha+eps))

%Bartlett Window Sequence
n=0:1:N-1;
wh=1−2∗𝑎𝑏𝑠(𝑛−𝑎𝑙𝑝ℎ𝑎)𝑁
hn=hd.*wh

% Plot the Band Stop Filter with Bartlett Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="663" height="513" alt="image" src="https://github.com/user-attachments/assets/23451898-a6bf-452e-be66-95bb6bbbbdce" />

## RESULT:
<img width="1443" height="653" alt="image" src="https://github.com/user-attachments/assets/4fa56daa-e9b6-4fad-9001-8cf628eed8bc" />

