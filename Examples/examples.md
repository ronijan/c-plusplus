### ex_01

```c++
#include <iostream>
using namespace std;

#define ROWS 5
#define COLS 3

int x, y;
char space = '\x09';

int main() {
	int arr[ROWS][COLS];
	
	for(x = 0; x <= COLS; x++){
		for(y = 0; y <= ROWS; y++){
			
			arr[ROWS][COLS] = rand() % 10; 
			
			cout << x << space << y << space << arr[ROWS][COLS] << endl;
			
		}
	}

	return 0;
}

output:
0	0	3
0	1	6
0	2	7
0	3	5
0	4	3
0	5	5
1	0	6
1	1	2
1	2	9
1	3	1
1	4	2
1	5	7
2	0	0
2	1	9
2	2	3
2	3	6
2	4	0
2	5	6
3	0	2
3	1	6
3	2	1
3	3	8
3	4	7
3	5	9
```

---

### ex_02

```c++
// C++ Program to find factorial of a number
// Factorial on n = 1*2*3*...*n

#include <iostream>
using namespace std;

int main() 
{
    int i, n, factorial = 1;

    cout << "Enter a positive integer: ";
    cin >> n;

    for (i = 1; i <= n; ++i) {
        factorial *= i;   // factorial = factorial * i;
    }

    cout<< "Factorial of "<<n<<" = "<<factorial;
    return 0;
}

output:
Enter a positive int:
9
Factorial of 9 = 362880

```

---

### ex_03

```c++

// C++ Program to compute factorial of a number
// Factorial of n = 1*2*3...*n

#include <iostream>
using namespace std;

int main() 
{
    int number, i = 1, factorial = 1;

    cout << "Enter a positive integer: ";
    cin >> number;
    
    while ( i <= number) {
        factorial *= i;      //factorial = factorial * i;
        ++i;
    }

    cout<<"Factorial of "<< number <<" = "<< factorial;
    return 0;
}
output:
Enter a positive int:
5
Factorial of 5 = 120

```

---


### ex_04

```c++
// C++ Program to demonstrate working of break statement

#include <iostream>
using namespace std;
int main() {
    float number, sum = 0.0;

    // test expression is always true
    while (true)
    {
        cout << "Enter a number: ";
        cin >> number;
        
        if (number != 0.0)
        {
            sum += number;
        }
        else
        {
            // terminates the loop if number equals 0.0
            break;
        }

    }
    cout << "Sum = " << sum;

    return 0;
}

output:
Enter a number: 1
Enter a number: 2
Enter a number: 3
Enter a number: 4
Enter a number: 5
Enter a number: 6
Enter a number: 7
Enter a number: 8
Enter a number: 9
Enter a number: 10
Enter a number: 0
Sum = 55

```

---


### ex_05

```c++

// Program to built a simple calculator using switch Statement

#include <iostream>
using namespace std;

int main()
{
    char o;
    float num1, num2;

    cout << "Enter an operator (+, -, *, /): ";
    cin >> o;

    cout << "Enter two operands: ";
    cin >> num1 >> num2;
    
    switch (o) 
    {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1+num2;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1-num2;
            break;
        case '*':
            cout << num1 << " * " << num2 << " = " << num1*num2;
            break;
        case '/':
            cout << num1 << " / " << num2 << " = " << num1/num2;
            break;
        default:
            // operator is doesn't match any case constant (+, -, *, /)
            cout << "Error! operator is not correct";
            break;
    }
    
    return 0;
}


output:
Enter an operator (+, -, *, /): *
Enter two operands: 5
5
5 * 5 = 25

```

---


### ex_06

```c++

// This program calculates the average of numbers entered by user.
// If user enters negative number, it ignores the number and 
// calculates the average of number entered before it.

# include <iostream>
using namespace std;

int main()
{
    float num, average, sum = 0.0;
    int i, n;

    cout << "Maximum number of inputs: ";
    cin >> n;

    for(i = 1; i <= n; ++i)
    {
        cout << "Enter n" << i << ": ";
        cin >> num;
        
        if(num < 0.0)
        {
           // Control of the program move to jump:
            goto jump;
        } 
        sum += num;
    }
    
jump:
    average = sum / (i - 1);
    cout << "\nAverage = " << average;
    return 0;
}

output:
Maximum number of inputs: 10
Enter n1: 3
Enter n2: 4
Enter n3: 5
Enter n4: 6
Enter n5: 7
Enter n6: 8
Enter n7: 94
Enter n8: 4
Enter n9: 3
Enter n10: 2
Average = 13.6

```

---


### ex_07

```c++
#include <iostream>
#include <cmath>

using namespace std;

int main()
{
    double number, squareRoot;
    cout << "Enter a number: ";
    cin >> number;

    // sqrt() is a library function to calculate square root
    squareRoot = sqrt(number);
    cout << "Square root of " << number << " = " << squareRoot;
    return 0;
}

output:
Enter a number: 7
Square root of 7 = 2.64575

```

---

### ex_08

```c++
# include <iostream>
using namespace std;

void prime();

int main()
{
    // No argument is passed to prime()
    prime();
    return 0;
}


// Return type of function is void because value is not returned.
void prime()
{

    int num, i, flag = 0;

    cout << "Enter a positive integer enter to check: ";
    cin >> num;

    for(i = 2; i <= num/2; ++i)
    {
        if(num % i == 0)
        {
            flag = 1; 
            break;
        }
    }

    if (flag == 1)
    {
        cout << num << " is not a prime number.";
    }
    else
    {
        cout << num << " is a prime number.";
    }
}

output:
Enter a positive integer enter to check: 7
7 is a prime number.

```

---


### ex_09

```c++

#include <iostream>
using namespace std;

void display(int);
void display(float);
void display(int, float);

int main() {

    int a = 5;
    float b = 5.5;

    display(a);
    display(b);
    display(a, b);

    return 0;
}

void display(int var) {
    cout << "Integer number: " << var << endl;
}

void display(float var) {
    cout << "Float number: " << var << endl;
}

void display(int var1, float var2) {
    cout << "Integer number: " << var1;
    cout << " and float number:" << var2;
}

output:
Integer number: 5
Float number: 5.5
Integer number: 5 and float number:5.5

```

---


### ex_10

```c++

#include <iostream>
using namespace std;

int main() {
  int min, max, i;
  float zahl = 0.0f;
  float zenArr[10];
  for(i = 0; i <= 9; i++){
     cout << "Gib 10 Zhalen ein!" << i+1 << "\n";
     cin >> zenArr[i];

     if(i == 0){
	min = zenArr[0];
	max = zenArr[0];
      }

      if(min > zenArr[i]){
	min = zenArr[i];
      }

      if(max < zenArr[i]){
	max = zenArr[i];
      }

      zahl = zahl+i;
  }

  zahl = zahl /10;

  cout << "Durchschnitt ist: " << zahl << "\n";
  cout << "Min ist: " << min << "\n";
  cout << "Max ist: " << max << "\n";
  return 0;
}

output:
Gib 10 Zhalen ein!1
1
Gib 10 Zhalen ein!2
6
Gib 10 Zhalen ein!3
6
Gib 10 Zhalen ein!4
6
Gib 10 Zhalen ein!5
6
Gib 10 Zhalen ein!6
6
Gib 10 Zhalen ein!7
5
Gib 10 Zhalen ein!8
4
Gib 10 Zhalen ein!9
90
Gib 10 Zhalen ein!10
766
Durchschnitt ist: 4.5
Min ist: 1
Max ist: 766

```

---

### ex_11

```c++

#include <iostream>
using namespace std;

int main() 
{
    int numbers[5], sum = 0;
    cout << "Enter 5 numbers: \n";
    
    //  Storing 5 number entered by user in an array
    //  Finding the sum of numbers entered
    for (int i = 0; i < 5; ++i) 
    {
        cin >> numbers[i];
        sum += numbers[i];
    }
    
    cout << "Sum = " << sum << endl;  
    
    return 0;
}

output:
Enter 5 numbers: 
1
1
1
5
5
Sum = 13

```
---


### ex_12

```c++

#include <iostream>
using namespace std;

int main() {
    string line;
    cout << "Enter a string: ";
    getline(cin, line);

    for(int i = 0; i < line.size(); ++i)
    {
        if (!((line[i] >= 'a' && line[i]<='z') || (line[i] >= 'A' && line[i]<='Z')))
        {
            line[i] = '\0';
        }
    }
    cout << "Output String: " << line << endl;    
    return 0;
}

output:
Enter a string: I_l98-3v_0_m
Output String: Ilvm

```

---

### ex_13

```c++


#include <iostream>
using namespace std;

int main() {
    char line[100], alphabetString[100];
    int j = 0;
    cout << "Enter a string: ";
    cin.getline(line, 100);

    for(int i = 0; line[i] != '\0'; ++i)
    {
        if ((line[i] >= 'a' && line[i]<='z') || (line[i] >= 'A' && line[i]<='Z'))
        {
            alphabetString[j++] = line[i]; 

        }
    }
    alphabetString[j] = '\0';

    cout << "Output String: " << alphabetString << endl;    
    return 0;
}


output:
Enter a string: _a.**b_##c000_d44
Output String: abcd

```

---


### ex_14

```c++

#include <iostream>
using namespace std;

int main()
{
    string s1, s2, result;

    cout << "Enter string s1: ";
    getline (cin, s1);

    cout << "Enter string s2: ";
    getline (cin, s2);

    result = s1 + s2;

    cout << "Resultant String = "<< result << endl;

    return 0;
}

output:
Enter string s1: C++ Programming
Enter string s2:   is awesome.
Resultant String = C++ Programming  is awesome.

```

---

### ex_15

```c++

#include <iostream>
using namespace std;

int main()
{
    string s1;

    cout << "Enter ur Name: ";
    getline (cin, s1);
    cout << "Ur Name = "<< s1 << endl;

    return 0;
}

output:
Enter ur Name: Jackie Jackie
Ur Name = Jackie Jackie
```
----
