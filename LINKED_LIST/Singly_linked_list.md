# SINGLY LINKED LIST
## Representation of SLL

```cpp
struct Node{
    int data;
    struct Node *next;
};
```
```cpp
typedef struc Node{
    int data;
    struct Node *next;
}Node;
```
```cpp
struct Node{
    int data;
    struct Node *next;
};
typedef struct Node Node;
```

## OPERATIONS on SLL

1.&emsp;**Creation** of empty Linked list

2.&emsp;**Traversal**  of a list

3.&emsp;**Searching**  an element in the list

4.&emsp;**Sorting** an element in the list

5.&emsp;**Inserting** an element in the list

&emsp;&emsp;a.&emsp;Insertion at **beginning**

&emsp;&emsp;b.&emsp;Insertion at **end**

&emsp;&emsp;c.&emsp;Insertion at a **particular position**

6.&emsp;**Deletion** of an element from the list

&emsp;&emsp;a.&emsp;Deletion from the **beginning**

&emsp;&emsp;b.&emsp;Deletion from the **end**

&emsp;&emsp;c.&emsp;Deletion a **particular Node**

&emsp;&emsp;d.&emsp;Deletion of **entire list**


## Implemention of SLL
```cpp
//singly Linked list
#include <stdio.h>
#include <stdlib.h>

//defining node
struct Node{
  int data;
  struct Node *next;
};

typedef struct Node Node;
Node *head=NULL;

//creating a Node
Node *createNode(int value){
    Node *temp=(Node *)malloc(sizeof(Node));
    temp->data=value;
    temp->next=NULL;
    return temp;
}
//creating a linked list
Node *createLinkedList(int value){
    Node *newNode=createNode(value);
    Node *temp=NULL;
    if(head==NULL){
        head=temp=newNode;
    }
    while(temp->next != NULL){
        temp=temp->next;
    }
    temp->next=newNode;
    return head;
}

void printList(){
    Node *temp=head;
    while(temp != NULL){
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL");
}

int main(){
    // Node *head=NULL;
    head=createLinkedList(10);
    head=createLinkedList(20);
    head=createLinkedList(30);
    head=createLinkedList(40);
    head=createLinkedList(50);
    
    printList();
    
    
    return 0;
}
```
