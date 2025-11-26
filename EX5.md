## Ex.No:5
## Ex.Name: Right rotate module of the red black tree
## Date:
## Aim:
To Write the Right rotate module of the red black tree in CPP.

## Algorithm:
Start the program.

In the main() function:

Create an object of Temperature.

Call the methods to read input, perform conversion, and display results.

Stop the program.

## Program:
```
void rightrotate(node* temp)
{
    node* left = temp->l;
    temp->l = left->r;
    
    if (temp->l)
        temp->l->p = temp;
        
    left->p = temp->p;
    
    if (!temp->p)
        root = left;
    else if (temp == temp->p->l)
        temp->p->l = left;
    else
        temp->p->r = left;
        
    left->r = temp;
    temp->p = left;
}
```
## Output:
<img width="1059" height="840" alt="image" src="https://github.com/user-attachments/assets/3fddcbb2-a4e9-442a-b9dd-828a36b4195c" />


## Result:
The Program Executed Successfully.
