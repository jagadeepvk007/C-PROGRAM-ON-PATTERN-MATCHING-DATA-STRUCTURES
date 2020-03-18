 #include<stdio.h>
 #include<conio.h>
 char str[50],pat[20],rep[20],ans[50];
  int c=0,m=0,i=0,k=0,j=0,flag=0;
   void read()
    {
     printf("enter the main string\n");
     scanf("%[^\n]s",str);
     printf("enter the pattern string\n");
     fflush(stdin);
     scanf("%s",pat);
     printf("enter the replace string\n");
     fflush(stdin);
     scanf("%s",rep);
    }

     void stringmatch()
      {
       while(str[c]!=NULL)
	{
	 if(str[m]==pat[i])
	  {
	   m++;
	   i++;
	    if(pat[i]==NULL)
	     {
	      flag=1;
	       for(k=0;rep[k]!=NULL;k++,j++)
	       ans[j]=rep[k];
	       i=0;
	       c=m;
	     }
	  }
      else
      {
       ans[j]=str[c];
       c++;
       j++;
       m=c;
       i=0;
     }
     ans[j]=NULL;
   }
  }

    void main()
     {
     clrscr();
     read();
     stringmatch();
     if(flag==1)
      printf("the resultant string is %s\n",ans);
     else
      printf("pattern not found\n");
       getch();
     }

