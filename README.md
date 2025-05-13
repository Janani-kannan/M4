# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int a;
    scanf("%d", &a);
    printf("After Left Shift Operation value of a is:%d\n", a << 2);
    printf("After Right Shift Operation value of a is:%d\n", a >> 2);

    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/dfc6ee3a-d634-4fa3-857c-9572d01fd2ee)



## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num1, num2;
    scanf("%d %d", &num1, &num2);
    int lastDigit1 = num1 % 10;
    int lastDigit2 = num2 % 10;
    if (lastDigit1 == lastDigit2) {
        printf("%d and %d are equal\n", lastDigit1, lastDigit2);
    }

    if (lastDigit1 != lastDigit2) {
        printf("%d and %d are not equal\n", lastDigit1, lastDigit2);
    }

    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/537ac378-ba03-4424-b40a-d1c324669a8f)


           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM

```
#include <stdio.h>

int main() {
    char str[100];
    int i = 0;
    fgets(str, sizeof(str), stdin); 
    do {
        if (str[i] >= 'A' && str[i] <= 'Z')
        {
            str[i] = str[i] + 32; 
        }
        i++;
    } while (str[i-1] != '\0');  

    printf("%s", str);

    return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/2e5469ce-aa93-4f46-954e-fd09f7306d9d)



## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM

```
#include <stdio.h>

int main() {
    char s[200];
    int count = 0, i;
    scanf(" %[^\n]", s);
    for (i = 0; s[i] != '\0'; i++) 
    {
        if ((i == 0 && s[i] != ' ') || (s[i] != ' ' && s[i - 1] == ' '))
            count++;
    }

    printf("%d\n", count);
    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/981bed9f-c1ad-48e0-b89c-71520649858f)




## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    char str1[100], str2[100];
    int i, flag = 0;
    scanf("%s", str1);
    scanf("%s", str2);
    for (i = 0; str1[i] != '\0' && str2[i] != '\0'; i++) {
        if (str1[i] != str2[i]) {
            flag = 1;
            break;
        }
    }

    if (flag == 0) {
        if (str1[i] == '\0' && str2[i] == '\0')
            printf("Both strings are equal\n");
        else if (str1[i] == '\0')
            printf("str1 is Less than str2\n");
        else
            printf("str2 is Less than str1\n");
    } else {
        if (str1[i] < str2[i])
            printf("str1 is Less than str2\n");
        else
            printf("str2 is Less than str1\n");
    }

    return 0;
}
```

## OUTPUT

 ![image](https://github.com/user-attachments/assets/afd7970b-16b1-4e3c-9486-31bccdcaf55c)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

