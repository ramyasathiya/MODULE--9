## Ex.No:4
## Ex.Name: Right Rotate Module of a Splay Tree
## Date:
## Aim:
To write a C++ program to perform a Right Rotation in a Splay Tree and display the tree before and after the rotation using preorder traversal.

## Algorithm:
Start the program.

Define a node structure with data, left, and right pointers.

Insert elements into the tree following Binary Search Tree (BST) insertion rules.

Implement a right rotate function that:

Makes the left child of a node the new root.

Adjusts pointers so that the original root becomes the right child of the new root.

Perform a splay operation on the given key using right rotation.

Display the tree traversal before and after the rotation.

Stop the program.

## Program:
```
node *rightRotate(struct node *x)
{
    node *y = x->left;
    x->left = y->right;
    y->right = x;
    return y;
}
```
## Output:
<img width="864" height="672" alt="image" src="https://github.com/user-attachments/assets/b8d3e481-a583-4d12-be00-20a70fb4d512" />




## Result:
The Program Executed Successfully.
