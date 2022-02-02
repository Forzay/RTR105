CODE

#include<stdio.h><br/>
#include<math.h><br/>

int main() {<br/>
 float a,c ,b ,x ,delta_x,funkca, funkcb, funkcx;<br/>
 int i=0;<br/>

  printf("Root solver: \n");<br/>

  printf("Please enter limit begining: ");<br/>
  scanf ("%f", &a);<br/>

  printf("Please enter limit end: ");<br/>
  scanf ("%f", &b);<br/>

  printf("Please enter precisity: ");<br/>
  scanf ("%e", &delta_x);<br/>

  printf("Please enter y: ");<br/>
  scanf ("%f", &c);<br/>

  funkca = sin(a)-c; funkcb = sin(b)-c;<br/>

  printf("sin(%7.3f)-%7.3f=%7.3f\t\t\t\t\t\t\t",a,c,funkca);<br/>
  printf("sin(%7.3f)-%7.3f=%7.3f\n",b,c,funkcb);<br/>

 while ((b-a)>delta_x){<br/>
  x = (a+b)/2.;<br/>
  if(funkca*(sin(x)-c)>0)<br/>
   a = x;<br/>
  else<br/>
   b = x;<br/>
  printf("sin(%7.3f)-%7.3f=%7.3f\t",a,c,funkca);<br/>
  printf("sin(%7.3f)-%7.3f=%7.3f\t",b,c,funkcb);<br/>
  printf("sin(%7.3f)-%7.3f=%7.3f\n",x,c,sin(x));<br/>
   i++;<br/>
 }<br/>

 printf("\nNumber of iterations: %d\n",i);<br/>
 printf("Root is at x=%.5f, because sin(x) is %.3f\n",x,sin(x));<br/>
 return 0;<br/>
}<br/>

TEST

![2labaTest1](https://user-images.githubusercontent.com/90374721/152211087-2e29894a-c8cd-4444-aaef-f63f321b0806.jpg)

![2LabaTest2](https://user-images.githubusercontent.com/90374721/152211208-653e1ed0-f5d2-45ec-9f2d-362fcc4c9d89.jpg)

