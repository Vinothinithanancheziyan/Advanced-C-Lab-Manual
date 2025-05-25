

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display stack elements using linked list.

Algorithm:

1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
struct Node   
{  
    char data[100];  
    struct Node *next;  
}*head;  
void display()  
{
    struct Node *current=head;
    while(current!=NULL)
    {
        printf("%s\n",current->data);
        current=current->next;
    }
}
```
Output:


![image](https://github.com/user-attachments/assets/02a4d1be-dedd-43f5-a19c-92c7b7e49b01)


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.

Aim:

To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node   
{  
    float data;  
    struct Node *next;  
}*head;  
void pop()  
{  
    struct Node *ptr=head;  
    if(head==NULL)  
    {  
        printf("stack is empty");  
    }  
    else  
    {  
        head=head->next;
        free(ptr);
        ptr=NULL;
    }  
}
```
Output:


![image](https://github.com/user-attachments/assets/bfb45b2b-3f0e-4da9-97ac-e2f76a175f0b)




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display queue elements using linked list.

Algorithm:

1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *current=front;
    if(front==NULL)
    {
        printf("queue is empty");
        return;
    }
    else
    {
        printf("Queue elements:\n");  
        while(current!=NULL)
        {
            printf("%.3f\n",current->data);
            current=current->next;
        }
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/dbd14b85-8a27-4602-b0a9-a123f61ad8ad)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *current=malloc(sizeof(struct Node));
    current->data=data;
    current->next=NULL;
    if(front==NULL)
    {
        front=rear=current;
    }
    else
    {
        rear->next=current;
        rear=current;
    }
}
```
Output:


![image](https://github.com/user-attachments/assets/8aedf8c2-4f8e-4dce-aca0-bae710b9d7bd)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
struct Node   
{  
    float data;  
    struct Node *next;  
}*head;
void peek()
{
    struct Node *current=head;
    printf("%.2f",current->data);
}
```
Output:

![image](https://github.com/user-attachments/assets/93c518cc-66c6-4da9-b89d-0a0c47c6d31d)

Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.

