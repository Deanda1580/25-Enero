# 25-Enero
Actividades de matlab 
%Ejercicio de Funciones
clear
clc

syms x1 x2 x3
fx1=2+sin(x1);
i=-10:0.1:-5;

fx2=exp(x2);
j=-5:0.1:2;

fx3=log(x3.^2+1);
k=2:0.1:10;

hold on
grid

Conversion1=subs(fx1,x1,i);
plot(i,Conversion1)

Conversion2=subs(fx2,x2,j);
plot(j,Conversion2)

Conversion3=subs(fx3,x3,k);
plot(k,Conversion3)

%//________________________________________________________



%Problema 1 Serie de Fibonaci
clear
clc

s=50;
v=zeros(1,s);

a=0;
b=1;
v(1)=1;
for n=2:s
    c=a+b;
    v(n)=c;
    a=b;
    b=c;
end

R=zeros(1,s-1);
R(1)=1;
for m=2:s-1
    R(m)=v(m+1)/v(m);
end

disp(R)

%//________________________________________________


%Script para resolver un sistema de ecuaciones
clc
clear

r=10;

A=[5 2*r r;
   3 6   2*r-1;
   2 r-1 3*r]

B=[2;
   3;
   5]

IA=inv(A)

Sol=IA*B

%//_____________________________________________________

%Comprobar que el Limite de la FunciÛn que tiende a Infinito es e 

clear
clc

n=[1 10 100 500 1000 2000 4000 8000];

f=zeros(1,8);

for i=1:8
    f(i)=(1+(1/n(i))).^n(i);
end

disp(f)


%//_______________________________________________



%CombinaciÛn de Matrices en una Matriz Diagonal de ellas mismas
clear
clc

A=[2 6;
   3 9]
B=[1 2;
   3 4]
C=[-5 5;
    5 3]

v=blkdiag(A,B,C)

%//_____________________________________________________

