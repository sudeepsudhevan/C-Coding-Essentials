# C Programming

1. **Print Hello World in C**
  
```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	puts("!!!Hello World!!!"); /* prints !!!Hello World!!! */
	return EXIT_SUCCESS;
}
```
This is a C program that prints `“!!!Hello World!!!”` to the standard output stream. Here is a line-by-line explanation of the code:

* `#include <stdio.h>`: This is a preprocessor directive that tells the compiler to include the header file `stdio.h`, which contains the declarations of input/output functions such as `printf()` and `puts()`.
* `#include <stdlib.h>`: This is another preprocessor directive that tells the compiler to include the header file `stdlib.h`, which contains the declaration of the macro `EXIT_SUCCESS`, which represents a successful termination of the program.
* `int main(void)`: This is the definition of the main function, which is the entry point of the program. The int keyword specifies the return type of the function, which is an integer. The void keyword inside the parentheses indicates that the function takes no arguments.
* `puts("!!!Hello World!!!");`: This is a function call that prints the string `“!!!Hello World!!!”` followed by a newline character to the standard output stream, which is usually the console or the terminal. The `puts()` function is defined in the `stdio.h` header file.
* `return EXIT_SUCCESS;`: This is a return statement that ends the execution of the main function and returns the value of EXIT_SUCCESS to the operating system. The `EXIT_SUCCESS` macro is defined in the `stdlib.h` header file and has a value of `0`, which indicates a successful termination of the program

2. **Input a Number and Print the number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a;
	printf("Enter a number");
	fflush( stdout );
		scanf("  %d",&a);
	printf("you have entered %d",a);

	return EXIT_SUCCESS;
}
```    
* `fflush(stdout);`: This is a function call that forces any buffered data in the standard output stream, which is usually the console or the terminal, to be written immediately. The `fflush()` function is defined in the `stdio.h` header file. The stdout macro represents the standard output stream. The purpose of this function is to ensure that the prompt message `"Enter a number"` is displayed before the user enters the input, as some systems may delay the output until a newline character is encountered.

3. **Sum of Two numbers**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int number1,number2,sum;
	printf("Enter two numbers"); /* prints enter two numbers */
	fflush( stdout );/*for printf to execute before scanf  */
	scanf("%d%d",&number1,&number2);
	sum=number1+number2;
	printf("Result is : %d",sum);

	return EXIT_SUCCESS;
}
```

4. **Average of Three number**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	float num1,num2,num3,avg;
	printf("Enter three number");
	fflush( stdout );
	scanf("%f%f%f",&num1,&num2,&num3);
	avg=(num1+num2+num3)/3;
	printf("average of 3 number is :%f",avg);
	return EXIT_SUCCESS;
}
```   

5. **Swapping With Temporary Variable**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a=10,b=21,temp;

	temp=a;
	a=b;
	b=temp;

	printf("a:%d  b:%d",a,b);
	return EXIT_SUCCESS;
}
```

6. **Swapping Without Temporary Variable**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int a=12,b=23;
	a=a+b;
	b=a-b;
	a=a-b;
	printf("a:%d  b:%d",a,b);
	return EXIT_SUCCESS;
}
```
   
7. **Input and Print Your name**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	char name;
	printf("Enter your name: ");
	fflush( stdout );
	scanf("%c",&name);
	printf("Your name is:%c",name);
	return EXIT_SUCCESS;
}
```     

8. **Sum of Two number with setbuf**

```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int number1;
	float number2;
	float sum;
	setbuf(stdout,NULL);
	printf("Enter two numbers: ");
	scanf("%d%f",&number1,&number2);
	sum=number1+number2;
	printf("sum is:%f",sum);
	return EXIT_SUCCESS;
}
```
* `setbuf(stdout,NULL);`: This is a function call that disables the buffering of the standard output stream, which is usually the console or the terminal. The `setbuf()` function is defined in the `stdio.h` header file. The stdout macro represents the standard output stream. The `NULL` macro represents a null pointer, which indicates no buffer is used. The purpose of this function is to ensure that the output is displayed immediately, without waiting for a newline character or a buffer flush .
  
