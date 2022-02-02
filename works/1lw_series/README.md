KODE

#include<stdio.h><br/>
#include<math.h>

void main(){<br/>
 long double x,y,a,s;<br/>
 int k=0;<br/>

 printf(" sin(x) solver \n");<br/>
 printf("Please enter value of (x): ");<br/>
 scanf("%Lf",&x);<br/>
 y = sin(x);<br/>
 printf("sin(%.2Lf)= %.2Lf\n",x,y);<br/>

 a = pow(-1,0)*pow(x,2*0+1)/(1);<br/>
 s += a;<br/>

 while (k<500)<br/>
 {<br/>
  if (k == 0)<br/>
   printf("a0 = %Le\tS0 =%.2Lf\n",a,s);<br/>
  k++;<br/>
  a = a*x/(k);<br/>
  s += a;<br/>
  if (k == 499)<br/>
   printf("a499 = %Le\tS499 =%.2Lf\n",a,s);<br/>
 }<br/>
 printf("a500 = %Le\tS500 =%.2Lf\n",a,s);<br/>

 printf("\n");<br/>
 printf("\t\t500\n");<br/>
 printf("\t\t----\n");<br/>
 printf("\t\t\\\t\t\n");<br/>
 printf("\t\t \\\t\tsin(x)\n");<br/>
 printf("y=\t\t|\t    ----------------\n");<br/>
 printf("\t\t /\t\t   k!\n");<br/>
 printf("\t\t/\n");<br/>
 printf("\t\t----\n");<br/>
 printf("\t\tk=0\n");<br/>

 printf("\n");<br/>
 printf("\t\t\tx\n");<br/>
 printf("R=\t\t   -----------\n");<br/>
 printf("\t\t\tk\n");<br/>
}

TEST

![image](https://user-images.githubusercontent.com/90374721/152209310-1ee6dd4a-dbcd-4ddc-8081-2003ad0e0b90.png)



![New Bitmap Image](https://user-images.githubusercontent.com/90374721/152207119-608ea102-54dd-43eb-9921-575edce7c137.jpg)
