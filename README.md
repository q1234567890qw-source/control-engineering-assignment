# control-engineering-assignment

# 제어공학 과제 3
**학번:** 2023732001  
**이름:** 임동현 

<img width="726" height="200" alt="image" src="https://github.com/user-attachments/assets/7757142f-525a-407a-b8c8-183f2636bbc8" />
 <img width="683" height="350" alt="image" src="https://github.com/user-attachments/assets/f2071f6f-0c4d-4b2c-8cc7-90b0ce57b503" />
<img width="737" height="697" alt="image" src="https://github.com/user-attachments/assets/d34cf3fb-dca0-4bbb-97b5-c02f6c86db17" />



<img width="760" height="611" alt="image" src="https://github.com/user-attachments/assets/26b8c2f5-df93-49d3-a6ff-58927e1da78d" />
<img width="488" height="702" alt="image" src="https://github.com/user-attachments/assets/d4f1ac1b-b357-4262-9157-2147f4194848" />




<img width="755" height="144" alt="image" src="https://github.com/user-attachments/assets/14d3eca3-0ea8-49df-9159-2439e38b48ce" />
<img width="900" height="251" alt="image" src="https://github.com/user-attachments/assets/b42a9415-8ff3-4416-bb28-b3393b5367e8" />
<img width="586" height="738" alt="image" src="https://github.com/user-attachments/assets/c3a28382-900a-4b22-a74b-17a6cbd80b25" />


<img width="562" height="200" alt="image" src="https://github.com/user-attachments/assets/6dc5e0d7-e524-4b8f-9ec8-8730d568a4be" />
<img width="566" height="701" alt="image" src="https://github.com/user-attachments/assets/23188a48-3c64-4940-8a44-dd57eda26b08" />
<img width="580" height="204" alt="image" src="https://github.com/user-attachments/assets/633de9da-642e-48b1-b50f-5f266d2464f5" />

clear; clc;

syms s t

X = [s, -1, 0;
     0, s, -1;
     48, 44, s+12];

% 역행렬 계산
X_inv = inv(X);

% 역행렬의 역라플라스 변환
X_inv_ilaplace = ilaplace(X_inv, s, t);

disp('X의 역행렬:');

disp(X_inv);

disp('역행렬의 역라플라스 변환:');

disp(X_inv_ilaplace);

<img width="1669" height="284" alt="image" src="https://github.com/user-attachments/assets/6620f90b-5cf6-4f03-a460-cfd01cae3e36" />


<img width="551" height="277" alt="image" src="https://github.com/user-attachments/assets/2673aeca-b14e-4315-a7b4-d93fcaa1f5e7" />
<img width="574" height="365" alt="image" src="https://github.com/user-attachments/assets/fe4b27d0-fafd-47b5-bdd8-a3619ea0914f" />

clc; clear; close all;

syms s

% 주어진 행렬
A = [1, 1, -1;
     4, 3,  0;
    -2, 1, 10];

B = [0; 0; 4];
C = [1, 0, 0];
D = 0;


% (sI - A)^(-1) 계산

Phi = inv(s*eye(3) - A);

% 전달함수 G(s) = C*(sI - A)^(-1)*B + D

G = C * Phi * B + D;


% 분자(n), 분모(d) 분리

[n, d] = numden(G);

n = expand(n);

d = expand(d);



% 결과 출력

disp('전달함수의 분자 (n):');
disp(n);
disp(' ');

disp('전달함수의 분모 (d):');
disp(d);
<img width="203" height="118" alt="image" src="https://github.com/user-attachments/assets/2da47faf-7112-41b2-8416-1bafbdeeec04" />

