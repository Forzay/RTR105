CODE

#include<stdio.h><br/>
#include<string.h><br/>

void main()<br/>
{<br/>
 char str[50], str2[50];<br/>
 char i = 0, moda = 0, x = 0,min=0,max=0,j=0,buf=0;<br/>
 long int av =0, med = 0, len = 0;<br/>
 printf("Please enter a sentence: ");<br/>
 scanf("%[^\n]s", str);<br/>
 strcpy(str2,str);<br/>
 len = strlen(str);<br/>
 for (i= 0;i < len - 1;i++){<br/>
  for (j= i+1; j < len;j++){<br/>
   if (str2[i] > str2[j]){<br/>
    buf = str2[i];<br/>
    str2[i] = str2[j];<br/>
    str2[j] = buf;<br/>
   }<br/>
  }<br/>
 }<br/>
  if (len%2 == 1)<br/>
   med = str2[len/2+1];<br/>
  if (len%2 == 0){<br/>
   med = str2[len/2]+str2[len/2+1];<br/>
   med /=2;<br/>
  }<br/>
 av/=len;<br/>
 max=str2[j-1];<br/>
 min=str2[0];<br/>

 printf("Alphabetic order - %s\n",str2);<br/>
 for (i= 0;str[i] != '\0' ;i++){<br/>
  x=str[i];<br/>
   av+=x;<br/>
 printf("%d ",str2[i]);<br/>
 }<br/>
 j=0;<br/>

 printf("Symbol amount - %ld\n",len);<br/>
 printf("Average - %ld\n",av);<br/>
 printf("Min = %d\n",min);<br/>
 printf("Max = %d\n",max);<br/>
 printf("Median = %ld\n",med);<br/>

 for (i=0;len > i ;i++){<br/>
 if (str2[i] == str2[i+1])<br/>
  j++;<br/>
 else if (str2[i] != str2[i+1])<br/>
  if(j > moda){ moda = j;<br/>
   j=0;<br/>
  }<br/>
 }<br/>
 j=0;<br/>

 for (i=0;len > i ;i++){<br/>
 if (str2[i] == str2[i+1])<br/>
  j++;<br/><br/>
 else if (str2[i] != str2[i+1]){<br/>
 if (moda==j){<br/>
   printf("Mode is %d\n", str2[i]);<br/>
   printf("----------------------------------\n");<br/>
 }<br/>
 j=0;}<br/>
}<br/>
}<br/>

TEST

![image](https://user-images.githubusercontent.com/90374721/152213026-25c93805-16b9-436a-970d-f27b477a8fa3.png)


