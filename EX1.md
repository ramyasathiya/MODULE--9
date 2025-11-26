## Ex.No:1
## Ex.Name: Search Module of the B+ Tree
## Date:
## Aim:
To write a C++ program to implement the Search Module of a B+ Tree and verify whether a given key is present in the tree.

## Algorithm:
Start the program.

Construct a B+ Tree from the given set of keys.

Insert keys level by level according to the rules of the B+ Tree.

Display the B+ Tree level-wise after construction.

Read the search key.

Traverse the tree:

Compare the search key with the keys in the current node.

If found, return success.

If not found, move to the appropriate child node.

Continue until the leaf node is reached.

If the key exists, display “Found” else display “Not Found”.

Stop the program.

## Program:
```
void BPTree::search(int x)
{
    if (root == NULL)
    {
    cout << "Tree is empty\n";
    }
    else
    {
        Node *cursor = root;
        while (cursor->IS_LEAF == false) 
        {
            for (int i = 0; i < cursor->size; i++)
            {
                if (x < cursor->key[i])
                {
                    cursor = cursor->ptr[i];
                    break;
                }
                if (i == cursor->size - 1) 
                {
                    cursor = cursor->ptr[i + 1];
                    break;
                }
            }
        }
        for (int i = 0; i < cursor->size; i++)
        {
            if (cursor->key[i] == x)
            {
                cout << "Found\n";
                return;
            }
         }
        cout << "Not found\n";
    }
}
```
## Output:

<img width="870" height="791" alt="image" src="https://github.com/user-attachments/assets/307bb103-8597-4ddd-8135-19a72c9fe627" />


## Result:
The Program Executed Successfully.
