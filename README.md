# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-
__AIM:__

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

__EQUIPMENTS NEEDED:__

.Computer with i3 Processor 

.SCI LAB 

__ALGORITHM:__

1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

__PROCEDURE:__ 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

__PROGRAM:__
```asm
clear;
clc;
clear;
function z = f(x)
    z = 3*(1 - x)^2
endfunction
a = 0;
b = 1;
EX = intg(a, b, f)
function z = c(y)
    z = 3*(1 - y)^2
endfunction
EY = intg(a, b, c)
function z = g(x)
    z = (x^2)*3*(1 - x)^2
endfunction
EX2 = intg(a, b, g)
function z = h(y)
    z = (y^2)*3*(1 - y)^2
endfunction
EY2 = intg(a, b, h)
vX2 = EX2 - (EX)^2
vY2 = EY2 - (EY)^2
disp(EX, "Mean of X =")
disp(EY, "Mean of Y =")
disp(vX2, "Variance of X =")
disp(vY2, "Variance of Y =")
x = input("Type in the reference sequence = ")
y = input("Type in the second sequence = ")
n1 = max(size(y)) - 1
r = corr(x, y, n1)
plot2d3('gnn', r)
```
__OUTPUT GRAPH:__
<img width="740" height="685" alt="image" src="https://github.com/user-attachments/assets/93682841-4b0d-4dcf-a235-df15c9314199" />
Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 4 6 8 10 11 12 13]
<img width="842" height="1280" alt="image" src="https://github.com/user-attachments/assets/59b2ece9-3ec7-4449-8090-b06764f374b4" />
<img width="811" height="1280" alt="image" src="https://github.com/user-attachments/assets/28e939ee-95fa-4947-856b-a3ae44a768fb" />
<img width="854" height="1280" alt="image" src="https://github.com/user-attachments/assets/b298e036-3dce-483f-8ccc-27cd9dc16bb3" />

__RESULT:__
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.

