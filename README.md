# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
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
### CALCULATIONS:
<img width="500" height="800" alt="WhatsApp Image 2026-08-08 at 12 28 46 AM" src="https://github.com/user-attachments/assets/2f2ce827-f747-4244-ba26-9edbf49c58b2" />


### SAMPLE OUTPUT:

<img width="765" height="673" alt="Screenshot 2026-07-28 084049" src="https://github.com/user-attachments/assets/9c7950b7-3c4c-4916-b2c5-55a6a6500b61" />



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

