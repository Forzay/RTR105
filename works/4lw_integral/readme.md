CODE

#include<stdio.h><br/>
#include<math.h><br/>
float f(float x);<br/>
void main(){<br/><br/>
 int k,n=2,m=1;<br/>
 float a=0.,b=0,h,delta_x=0,int1=0.,int2=0.,int3=0.;<br/>

  printf("Integer solver:\n");<br/>

  printf("Please enter limit starting point: ");<br/>
  scanf ("%f", &a);<br/>

  printf("Please enter limit end point: ");<br/>
  scanf ("%f", &b);<br/>

  printf("Please enter precisity: ");<br/>
  scanf ("%e", &delta_x);<br/>

  int2 = (b-a)*(sin(a)+sin(b))/2.;<br/>

 while(fabs(int2 - int1)>delta_x){<br/>
  n*=2;<br/>
  h=(b-a)/n;<br/>
  int1=int2;<br/>
  int2=0.;<br/>
 for(k=0;k<n;k++) int2+=h*sin(a+(k+0.5)*h);<br/>
 }<br/><br/>
 printf("\nInteger solver with Riemann sum: %.5f\n",int2);<br/>

 int1 =0;<br/>
 int2 = (b-a)*(sin(a)+sin(b))/2.;<br/>
 while(fabs(int2 - int1)>delta_x){<br/>
  m*=2;<br/>
  n=2*m;<br/>
  h=(b-a)/n;<br/>
  int1=int2;<br/>
  int2=0.;<br/>
 for(k=1;k<=m-1;k++) int2+=2.*(2*sin(a+(2*k-1)*h)+sin(a+2*k*h));<br/>
 int2+=sin(a)+sin(b)+4*sin(b-h);<br/>
 int2*=h/3;<br/>
 }
 printf("Integer solver with Simpson method: %.5f\n",int2);<br/>

 n =2;<br/>
 int1 =0;<br/>
 int2 = (b-a)*(sin(a)+sin(b))/2.;<br/>
 while(fabs(int2 - int1)>delta_x){<br/>
  n*=2;<br/>
  h=(b-a)/n;<br/>
  int1=int2;<br/>
  int2=0.;<br/>
 for(k=1;k<n;k++) int2+=sin(a+(k)*h);<br/>
 int2+=(sin(b)+sin(a))/2;<br/>
 int2*=h;<br/>
 }<br/>
 printf("Integer solve with trapezoidal rule: %.5f\n",int2);<br/>

}<br/>

float f(float x){<br/>
 float y1;<br/>
 y1 = (1+x)*exp(x);<br/>
 return y1;<br/>
}<br/>

TEST

![4Laba](https://user-images.githubusercontent.com/90374721/152212517-e8d02078-bec8-431a-8088-912d16ba4f19.jpg)
