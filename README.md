# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
```
clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
for k=0:N-1
for n=0:N-1
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle = atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum')
```
### DFT DIRECT METHOD
### CALCULATIONS:
<img width="832" height="1280" alt="image" src="https://github.com/user-attachments/assets/9002cf55-6fd8-4a2a-bc68-58c461bc750e" />

### SAMPLE OUTPUT:
<img width="762" height="627" alt="image" src="https://github.com/user-attachments/assets/35594a7e-81c9-40a3-bb34-e3b9f7721824" />



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

