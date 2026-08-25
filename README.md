# FIR-FILTER-DESIGN
# EXP 4 c: Design-of-FIR-Digital-Filter-using-Hanning-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Hanning-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=Wc/%pi;
else
hd(n)=sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.5-(0.5*cos((2*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR LPF using Hanning Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR LPF using Hanning Window');
```
# OUTPUT: 
<img width="717" height="572" alt="image" src="https://github.com/user-attachments/assets/29bb556c-b93c-4a91-b8bb-12c427690155" />


# RESULT: 

Thus design of low pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=1-Wc/%pi;
else
hd(n)=-sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.5-(0.5*cos((2*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR HPF using Hanning Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR HPF using Hanning Window');
```
# OUTPUT: 
<img width="703" height="587" alt="image" src="https://github.com/user-attachments/assets/23b2ba6e-f5eb-4f95-afb2-34061ca7bfde" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=(Wc2-Wc1)/%pi;
else
hd(n)=(sin(Wc2*((n-1)-alpha))-sin(Wc1*((n-1)-alpha)))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.5-(0.5*cos((2*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR BPF using Hanning Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR BPF using Hanning Window');
```
# OUTPUT: 
<img width="710" height="582" alt="image" src="https://github.com/user-attachments/assets/728fb5d3-cd38-4f39-a3e5-4b6dcc28e864" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;
M=input('Enter the Odd Filter Length =');
Wc=input('Enter the Digital Cut off frequency =');
Wc2=Wc(2);
Wc1=Wc(1);
alpha=(M-1)/2;
for n=1:M
if (n==alpha+1) then
hd(n)=1-((Wc2-Wc1)/%pi);
else
hd(n)=(sin(Wc1*((n-1)-alpha))-sin(Wc2*((n-1)-alpha)))/(((n-1)-alpha)*%pi);
end
end
for n=1:M
W(n)=0.5-(0.5*cos((2*%pi*(n-1))/(M-1)));
end
h=hd.*W;
disp(h,'Filter Coefficients are');
[hzm,fr]=frmag(h,256);
subplot(2,1,1);
plot(2*fr,hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR BSF using Hanning Window');
hzm_dB=20*log10(hzm);
subplot(2,1,2);
plot(2*fr,hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR BSF using Hanning Window');
```
# OUTPUT: 
<img width="717" height="580" alt="image" src="https://github.com/user-attachments/assets/0c3ae832-537c-45a5-8293-46bedc8e70cf" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Hanning-Window waveforms were plotted and output was verified.
