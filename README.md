# Matlab_6

clear 
nneg=-10:-1; % variable para los numeros negativos
npos=1:10; %npos variable para los numeros positivos 
Fnneg=(1./(j*nneg*pi)).*(-3*exp(-j*nneg*6*pi/7)+2*exp(j*nneg*2*pi/7)+exp(-j*nneg*12*pi/7));
Fnpos=(1./(j*npos*pi)).*(-3*exp(-j*npos*6*pi/7)+2*exp(j*npos*2*pi/7)+exp(-j*npos*12*pi/7)); 
%Fnneg funcion para los numeros negativos (resuelve la expresion exponencial de la serie de Fourier)
%Fnpos funcion para los numeros pos (resuelve la expresion exponencial de la serie de Fourier)
F0=10/7; 
n=[nneg, 0, npos]; %contenedor de numeros en un rango
Fn=[Fnneg, F0, Fnpos];%contenedor de las funciones 
stem(n, abs(Fn)) %grafica  la amplitud del espectro.
stem(n*(1/7),abs(Fn))
