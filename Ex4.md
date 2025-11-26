# Ex.No:4
# Ex.Name: Write a CPP Program to insert five float elements in to Queue ADT (use STL for Queue)
## Date:
## Aim:
To write a C++ program to insert five float elements into a queue using the STL queue container.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include the <iostream> and <queue> headers.

STEP 3: Declare a queue of type float.

STEP 4: Read five float values from the user.

STEP 5: Use the push() function to insert each value into the queue.

STEP 6: Display a message indicating that elements are inserted.

STEP 7: Use a loop to display the elements of the queue using front() and pop().

STEP 8: Remove elements from the queue after displaying (optional).

STEP 9: End the program.

STEP 10: Verify the program to ensure all elements are inserted correctly and queue follows FIFO principle




## Program:
```
#include <iostream>
#include <queue>
using namespace std;

int main()
{
    queue<float> myQueue;
    float element;
    
    for (int i = 0; i < 5; ++i)
    {
        cin >> element;
        myQueue.push(element);
    }
    
    cout << "Queue Elements are:";
    
    while (!myQueue.empty()) 
    {
        cout << myQueue.front() << " ";
        myQueue.pop();
    }
    
    cout << endl;
    return 0;
}
```


## Output:
<img width="1167" height="311" alt="{E149026D-9169-4249-AE62-C558E41082F4}" src="https://github.com/user-attachments/assets/5ae02ba2-3ab2-413c-be4c-d165403805ea" />



## Result:
The program successfully inserts five float elements into the queue and demonstrates the FIFO (First In First Out) behavior of the queue.
