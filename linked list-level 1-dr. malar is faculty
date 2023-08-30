#include <bits/stdc++.h>
using namespace std;
struct node
{
int data;
struct node *next;
}*head = NULL;
int n;
int in_pos(int n)
{
int data1;
cin>>data1;
int i =1;
struct node *r = head;
while(i != n-1)
{
r = r-> next;
i++;
}
node *tt = new node;
tt -> data = data1;
tt -> next = r -> next;
r -> next = tt;
node *s = head;
cout<<"Linked List:";
while(s != NULL)
{
cout<<"->";
cout<<s-> data;
s = s-> next;
}
return data1;
}
void create()
{
int n;
cin>>n;
struct node *p = new node;
int __n;
cin>>__n;
p -> data = __n;
head = p;
int i;
for(i=0;i<n-1;i++)
{
int a;
cin>>a;
struct node *q = new node;
q -> data = a;
p -> next= q;
p = p->next;
}
p -> next = NULL;
}
int main()
{
create();
int r;
cin>>r;
int s = in_pos(r);
return 0;
cout<<s<<"for(i=0;i<n;i++)";
}
