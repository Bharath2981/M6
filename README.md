# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main()
{
    float length, breadth, area;
    float *ptr1, *ptr2;

    printf("Enter the length of the rectangle: ");
    scanf("%f", &length);
    printf("Enter the breadth of the rectangle: ");
    scanf("%f", &breadth);

    ptr1 = &length;
    ptr2 = &breadth;

    area = (*ptr1) * (*ptr2);

    printf("Area of Rectangle = %.2f\n", area);

    return 0;
}
```
## OUTPUT
		       	
![alt text](<Screenshot 2025-10-21 105917.png>)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
int main(){
    int n;scanf("%d",&n);
    char * str = (char*) malloc(n*sizeof(char));
    scanf("%s",str);
    printf("%s",str);
    free(str);
}
```
## OUTPUT

![alt text](<Screenshot 2025-10-21 121234.png>)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct Student
{
    int rollno;
    char name[50];
    float marks;
};

int main()
{
    struct Student s;

    printf("Enter roll number: ");
    scanf("%d", &s.rollno);

    printf("Enter name: ");
    scanf("%s", s.name);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Details\n");
    printf("Roll Number: %d\n", s.rollno);
    printf("Name: %s\n", s.name);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```

## OUTPUT

![alt text](<Screenshot 2025-10-21 121359.png>)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct em{
    int n;
    char d[100];
    int bp;
    int da;int hra;
    float gs;
}e[3];
int main(){
    for (int i=0;i<3;i++){
        scanf("%d",&e[i].n);
        scanf("%s",e[i].d);
        scanf("%d",&e[i].bp);
        e[i].da=e[i].bp*0.1;e[i].hra=e[i].bp*0.3;
        e[i].gs=e[i].bp+e[i].da+e[i].hra;
    }
    printf("Details of the Employee:\n");
    for (int i=0;i<3;i++){
        printf("%d %s %d %d %d %.2f\n",e[i].n,e[i].d,e[i].bp,e[i].da,e[i].hra,e[i].gs);
    }
}
```

 ## OUTPUT

 ![alt text](<Screenshot 2025-10-21 121544.png>)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
struct mark{float t;float p;}; 
struct std{
    int n;int a,b,c;
    struct mark m;
}s[5];

int main(){
    for (int i=0;i<5;i++){
        scanf("%d\n%d\n%d\n%d",&s[i].n,&s[i].a,&s[i].b,&s[i].c);
        s[i].m.t=s[i].a+s[i].b+s[i].c;
        s[i].m.p=s[i].m.t/3;
    }
    printf("Student Details are\n");
    for (int i=0;i<5;i++){
        printf("%d       %d       %d       %d       %.2f       %.2f\n",s[i].n,s[i].a,s[i].b,s[i].c,s[i].m.t,s[i].m.p); 
    }
    
}
```

## OUTPUT

 ![alt text](<Screenshot 2025-10-21 121944.png>)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


