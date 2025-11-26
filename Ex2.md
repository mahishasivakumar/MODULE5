# Ex.No:2
# Ex.Name: Write a C++ Program to Check for balanced parenthesis by using Stack STL
## Date:
## Aim:
To write a C++ program to check whether parentheses in a given expression are balanced using the stack STL.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include <iostream> and <stack> libraries.

STEP 3: Read the expression containing parentheses from the user.

STEP 4: Declare a stack of characters.

STEP 5: Traverse each character of the expression.

STEP 6: If the character is an opening parenthesis '(', push it onto the stack.

STEP 7: If the character is a closing parenthesis ')', check if the stack is empty.

If empty → parentheses are unbalanced.

Otherwise → pop the top element from the stack.

STEP 8: After traversing the expression, check if the stack is empty.

If empty → parentheses are balanced.

Otherwise → parentheses are unbalanced.

STEP 9: Display the result to the user.

STEP 10: End the program.




## Program:
```
#include<iostream>
#include<stack>
#include<string>
using namespace std;
bool isbalanced(const string &expression){
    stack<char>s;
    for(char ch : expression){
        if(ch=='(' || ch=='{' || ch=='['){
            s.push(ch);
        }
        else if ( ch=='}' || ch==')' || ch==']'){
            if(s.empty()){
                return false;
            }
            char top=s.top();
            s.pop();
            if((ch==')' && top!='(') || (ch==']' && top!='[' )|| (ch=='}' && top!='{' )){
                return false;
            }
        }
    }
    return s.empty();
}
int main(){
    string expression;
    cin>>expression;
    if(isbalanced(expression)){
        cout<<"Balanced";
    }
    else{
        cout<<"Not Balanced";
    }
}

```


## Output:
<img width="499" height="247" alt="{B1E826A5-5227-4D3C-AA30-2947CB9F9F0A}" src="https://github.com/user-attachments/assets/065b8f82-ce5a-4d56-aaf4-a3d447a23625" />



## Result:
The program correctly identifies whether the parentheses in the given expression are balanced or not balanced.

