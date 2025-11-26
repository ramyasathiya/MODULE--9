## Ex.No:2
## Ex.Name: Red-Black Tree Construction Module
## Date:
## Aim:
To write a C++ program to construct a Red-Black Tree (RBT) and display its inorder traversal along with node colors.

## Algorithm:
1.Start the program.

2.Define a Red-Black Tree node structure with:

Data (key value)
Color (0 = Black, 1 = Red)

3.Left and Right child pointers, Parent pointer.

4.Insert nodes one by one into the tree following the Binary Search Tree (BST) property.

5.After each insertion, perform fix-up operations to maintain Red-Black Tree properties:
Root must always be black.
No two red nodes can appear consecutively.
Every path from root to leaf must contain the same number of black nodes.
Perform rotations (Left Rotate, Right Rotate) and recoloring when violations occur.

6.Once all elements are inserted, perform Inorder Traversal to display:
Node data
Node color (0 = Black, 1 = Red).

7.Stop the program.

## Program:
```
node* bst(node* trav, node* temp)
{
    if (trav == NULL)
        return temp;
    if (temp->d < trav->d)
    {
        trav->l = bst(trav->l, temp);
        trav->l->p = trav;
    }
    else if (temp->d > trav->d)
    {
        trav->r = bst(trav->r, temp);
        trav->r->p = trav;
    }
    return trav;
}
```
## Output:

<img width="1348" height="861" alt="image" src="https://github.com/user-attachments/assets/91c92df4-50f2-44fe-b824-d37a28c04f03" />




## Result:
The Program Executed Successfully.
