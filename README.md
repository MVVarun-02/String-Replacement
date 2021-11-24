# String-Replacement
Replacing a pattern sting in main string with replacement string.

#include <stdio.h>

#include <stdlib.h>


void main() {

  char STR[100];
  
  char PAT[100];
  
  char REP[100];
  
  char RES[100];
  
  int i=0;
  
  int j=0;
  
  int c=0;
  
  int m=0;
  
  int k;
  
  int flag=0;
  

  printf("Enter the main string: \n");
  
  gets(STR);
  
  printf("Enter a pattern string: \n");
  
  gets(PAT);
  
  printf("Enter a replace string: \n");
  
  gets(REP);
  
  while (STR[c] != '\0') {                          /* '/0' represents null terminator*/
  
    if (STR[m] == PAT[i]) {
    
      i++;
      
      m++;
      
      if ( PAT[i] == '\0') {
      
        for(k=0; REP[k] != '\0';k++,j++) {
        
          RES[j] = REP[k];
          
          flag=1;
          
        }
        
        i=0;
        
        c=m;
        
      }
      
    }
    
    else {
    
      RES[j] = STR[c];
      
      j++;
      
      c++;
      
      m=c;
      
      i=0;
      
    }
    
  }
  
  if(flag==0) {
  
    printf("Pattern is not found\n");
    
  }
  
  else {
  
    RES[j] = '\0';
    
    printf("The resultant string is:%s\n" ,RES);
    
  }
  
}
