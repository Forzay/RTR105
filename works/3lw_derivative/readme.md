CODE<br/>

#include<stdio.h><br/>
#include<math.h><br/>
void data_table_in_file(int k,float a,float b, float delta_x);<br/>
double function(double x, double x1,double delta_x);<br/>

void main(){<br/>
 int k=0;<br/>
 float a=0.,b=0,x,delta_x=1.e-2;<br/>

  printf("Please enter starting limit: ");<br/>
  scanf ("%f", &a);<br/>

  printf("Please enter end limit: ");<br/>
  scanf ("%f", &b);<br/>

  printf("Please enter precisity: ");<br/>
  scanf ("%e", &delta_x);<br/>

  x=a;<br/>
  while(x<=b){<br/>
  k++;<br/>
  x+= delta_x;<br/>
  }<br/>
 data_table_in_file(k,a,b,delta_x);<br/>
}<br/>
double function(double x, double x1,double delta_x){<br/>
float y;<br/>
 y= (x1-x)/delta_x;<br/>
	return y;<br/>
}<br/>

void data_table_in_file(int k,float a,float b, float delta_x){<br/>
int i;<br/>
float x[k],y1[k],y2[k],y3[k],y4[k],y5[k];<br/>
 FILE *fp = fopen("./please work.dat", "w");<br/>
 fprintf(fp,"\tx\t\tf(x)\t\tf\'(x)\t\tf\"(x)\t\tf\'(x)\t\tf\"(x)\n");<br/>

 for(i=0;i<k;i++){<br/>
 if (i==0)<br/>
  x[i]=a;<br/>
 else<br/>
  x[i] = x[i-1] + delta_x;<br/>
 y1[i] = (1+x[i])*exp(x[i]);<br/>
 y2[i] = (2+x[i])*exp(x[i]);<br/>
 y3[i] = (3+x[i])*exp(x[i]);<br/>
 }<br/>

 for(i=0;i<(k-1);i++)<br/>
  y4[i]= function(y1[i],y1[i+1],delta_x);<br/>


 for(i=0;i<(k-2);i++)<br/>
  y5[i] = function(y2[i],y2[i+1],delta_x);<br/>
  for(i=0;i<k;i++)<br/>
   fprintf(fp,"%10.2f\t%13.2f\t%13.2f\t%13.2f\t%13.2f\t%13.2f\n",x[i],y1[i],y2[i],y3[i],y4[i],y5[i]);<br/>
 fclose(fp);<br/>
}<br/>

TEST

![image](https://user-images.githubusercontent.com/90374721/152211881-c9e0e185-1624-42b4-87da-d3fa084546c8.png)

![3Laba](https://user-images.githubusercontent.com/90374721/152211958-561dba68-f7e6-4b73-add2-acd4ee1d680b.jpg)

