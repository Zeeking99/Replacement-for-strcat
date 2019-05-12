/*

    This program is to demonstrate the use of fstrcat(). 
    I created this function because the original strcat() is susceptible to bufferoverflow 
    if the size of the str1 is not big enough to accomodate the str2
    
    The function will return an address to the combined string or else if sufficient memory is not allocated it will 
    return 1.
    
*/    

char * fstrcat(char * str1, char * str2);

#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main() 
{
    char string1[10] = "Uzma ",string2[10] = "Sadia";
    char * string;
    
    string = fstrcat(string1,string2);
    printf("%s",string);
    
    free(string);
    return 0;
}


char * fstrcat(char * str1, char * str2)
{
    int strlen1, strlen2, combinedlen;
    char * combinedstr;
    
    strlen1 = strlen(str1);
    strlen2 = strlen(str2);
    
    combinedlen = strlen1+strlen2;
    combinedstr = (char *)malloc((combinedlen+1)*sizeof(char)); // allocating memory with the length of two strings combined
    
    if(combinedstr == NULL)
        return 1;
    
    combinedstr = strcat(combinedstr,str1);
    combinedstr = strcat(combinedstr,str2);
    
    return combinedstr;
}
