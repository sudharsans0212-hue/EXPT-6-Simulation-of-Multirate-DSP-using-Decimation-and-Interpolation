# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

# To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```sci
clear;
clc;
close;

// Generate the original signal
n = 0:%pi/50:2*%pi;
x = sin(%pi * n);

// Input factors
M = input("Enter the Downsampling Factor (M): ");
L = input("Enter the Upsampling Factor (L): ");

//-------------------------
// Downsampling
//-------------------------
downsampling_x = x(1:M:length(x));

disp(x, "Input Signal x(n) = ");
disp(downsampling_x, "Downsampled Signal = ");

// Plot Original and Downsampled Signals
figure(1);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(downsampling_x), downsampling_x);
xtitle("Downsampled Signal by a Factor of M");

//-------------------------
// Upsampling
//-------------------------
upsampling_x = zeros(1, L * length(x));

for i = 1:length(x)
    upsampling_x(1, L*i) = x(i);
end

disp(x, "Input Signal x(n) = ");
disp(upsampling_x, "Upsampled Signal = ");

// Plot Original and Upsampled Signals
figure(2);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(upsampling_x), upsampling_x);
xtitle("Upsampled Signal by a Factor of L");
```
# OUTPUT: 

<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/b3b241d4-f4a2-4fb2-a83a-23e2a3fa00f2" />
<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/8fc2349a-ea14-4ab3-9df2-beb9da6d00e8" />

# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
