# Ex.No:1
# Ex.Name: Write a CPP Program to insert five double elements in to Stack ADT (use STL for Stack)
## Date:
## Aim:
To write a C++ program to insert five double elements into a stack using the STL stack container.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include the <stack> and <iostream> headers.

STEP 3: Declare a stack of type double.

STEP 4: Read five double values from the user.

STEP 5: Use the push() function to insert each value into the stack.

STEP 6: Display a message that the elements are inserted.

STEP 7: Optionally, display the stack elements using a loop and top() function.

STEP 8: Pop elements from the stack after displaying (if needed).

STEP 9: End the program.

STEP 10: Verify the program to ensure all elements are inserted correctly.




## Program:
```
#include <iostream>
#include <stack>

using namespace std;

int main() 
{
    int n;
    cin >> n;
    stack<float> stk;
    float num;

    for (int i = 0; i < n; ++i)
    {
        cin >> num;
        stk.push(num);
    }

    cout << "Size of the stack: " << stk.size() << endl;

    while (!stk.empty())
    {
        cout << stk.top() << " ";
        stk.pop();
    }
    
    cout << endl;
    return 0;
}

```


## Output:
<img width="877" height="308" alt="{1A080251-6945-4DDF-BBFC-DD7312EF99A1}" src="https://github.com/user-attachments/assets/403803b1-be41-4c49-983b-9a1c67de9734" />



## Result:
The program successfully inserts five double elements into the stack using STL and demonstrates the LIFO (Last In First Out) property of a stack.
