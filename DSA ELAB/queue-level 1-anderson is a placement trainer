#include <stdio.h>
#include <stdlib.h>
struct node *f = NULL;
struct node *r = NULL;
struct node
{
 int data;
 struct node* next;
};
void enqueue(int d)
{
 struct node *n;
 n = (struct node*)malloc(sizeof(struct node));
 if(n==NULL){
 printf("Queue is Full");
 }
 else{
 n->data = d;
 n->next = NULL;
 if(f==NULL){
 f=r=n;
 }
 else{
 r->next = n;
 r=n;
 }
 }
}
int dequeue()
{
 int val = -1;
 struct node* t;
 t = f;
 if(f==NULL){
 printf("Queue is Empty\n");
 }
 else{
 f = f->next;
 val = t->data;
 free(t);
 }
 return val;
}
int main()
{
 int n,i,t;
 scanf("%d",&n);
 for(i=0;i<n;i++)
 {
 scanf("%d",&t);
 enqueue(t);
 }
 for(i=0;i<n;i++){
 printf("%d\n",dequeue());
 }
 return 0;
}
