## Linear Algebra Examples

Linear System Example: One,No,Many Solutions
```markdown
clear 
close all
resx=-5:0.1:5;

%%----------------------One solution / Intersection---------------------- 
% 4x + 3y =2
% 7x + 5y =3

y1 =(4*resx-2)/3;
y2 =(7*resx-3)/5;

L1=[[4 3];[7 5]];
C1=[2;3];
det(L1)
U1=linsolve(L1,C1)

figure(1)
plot(y1);hold on;
plot(y2);hold on;
xlabel('x'); ylabel('y'); grid on;
title('Exactly one solution')

%%----------------------No solution / Parallel Line---------------------- 
% 2x + 4y =3
% 3x + 6y =2

y3=(2*resx -3)/4;
y4=(3*resx -2)/6;

L2=[[2 4];[3 6]];
C2=[3;2];
det(L2)
U2=linsolve(L2,C2)

figure(2)
plot(y3);hold on;
plot(y4);hold on;
xlabel('x'); ylabel('y'); grid on;
title('No solution')

%%----------------------Infinitesmally many solutions / Overlap ---------------------- 
% 2x + 4y =2
% 3x + 6y =3

y5=(2*resx -2)/4;
y6=(3*resx -3)/6;

L3=[[2 4];[3 6]];
C3=[2;3];
det(L3)
U3=linsolve(L3,C3)

figure(3)
plot(y5);hold on;
plot(y6);
xlabel('x'); ylabel('y'); grid on;
title('Infinitesmally many solution')
```
