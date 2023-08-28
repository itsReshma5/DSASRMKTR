#include <bits/stdc++.h>
using namespace std;
struct Node
{
int data;
struct Node *next;
struct Node *prev;
};
void insertStart(struct Node** head,int data)
{
 struct Node* new_node = new Node();
 new_node->data = data;
 new_node->next = (*head);
 new_node->prev = NULL;
 if ((*head) != NULL)
 (*head)->prev = new_node;
 (*head) = new_node;
}
void printList(struct Node* node)
{
Node* last;
while (node != NULL)
{
cout<<node->data<<" ";
last = node;
node = node->next;
}
cout<<endl;
while (last != NULL)
{
cout<<last->data<<" ";
last = last->prev;
}
}
int main()
{
struct Node* head = NULL;
int n;
cin>>n;
for(int i=0;i<n;i++){
 int t;
 cin>>t;
 insertStart(&head, t);
}
printList(head);
return 0;
}
