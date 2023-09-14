#include <stdio.h>
#include <stdlib.h>
int compare(const void *a, const void *b);
int search(int* arr,int value,int start,int end);
int main()
{
 int i,n, q, t, id;
 int one = 0, len = 0, qu_rear = 0, front = 0, b;
 int idx[3][200002], sol[400001] = {0}, queue[200002], answer[2], **sol2;
 scanf("%d %d", &n, &q);
 for (i = 0; i < n; i++){
 idx[1][i] = 0;
 idx[2][i] = 3;
 }
 for(i = 0;i < n;i++){
 int a, d;
 scanf("%d %d", &a, &d);
 idx[0][i] = a + d;
 sol[len] = a + d;
 len++;
 if (d != 0 && a - d > 0){
 idx[1][i] = a - d;
 sol[len] = a - d;
 len++;
 }
 }
 qsort(sol, len, sizeof(int), compare);
 for (i = 0; i < 2 * n; i++){
 if (sol[i] != 0 && sol[i] == sol[i + 1])
 sol[i] = 0;
 }
 len = 0;
 for (i = 0; i < 2 * n; i++) {
 if (sol[i] != 0) {
 sol[len] = sol[i];
 len++;
 }
 }
 sol[len] = 0;
 sol2 = calloc(2, sizeof(int *));
 for (i = 0; i < 2; i++){
 sol2[i] = calloc(1 + len, sizeof(int));
 }
 for (i = 0; i < n; i++) {
 if (idx[0][i] == 0){
 idx[0][i] = len;
 }
 else {
 idx[0][i] = search(sol, 0, len - 1, idx[0][i]);
 }
 }
 for (i = 0; i < n; i++) {
 if (idx[1][i] == 0){
 idx[1][i] = len;
 }
 else{
 idx[1][i] = search(sol, 0, len - 1, idx[1][i]);
 }
 }
 for (i = 0; i < q; i++){
 scanf("%d %d", &t, &id);
 id = id - 1;
 if (t == 1 && idx[2][id] != t){
 if (idx[2][id] == 2){
 sol2[1][idx[0][id]]--;
 sol2[1][idx[1][id]]--;
 }
 one++;
 queue[qu_rear++] = id;
 sol2[0][idx[0][id]]++;
 sol2[0][idx[1][id]]++;
 }
 else if (t == 2 && idx[2][id] != t) {
 if (idx[2][id] == 1){
 sol2[0][idx[0][id]]--;
 sol2[0][idx[1][id]]--;
 one--;
 }
 sol2[1][idx[0][id]]++;
 sol2[1][idx[1][id]]++;
 }
 else if (t == 3){
 if (idx[2][id] == 1){
 one--;
 sol2[0][idx[0][id]]--;
 sol2[0][idx[1][id]]--;
 }
 else if (idx[2][id] == 2){
 sol2[1][idx[0][id]]--;
 sol2[1][idx[1][id]]--;
 }
 }
 idx[2][id] = t;
 if (one == 0){
 printf("-1\n");
 }
 else{
 answer[0] = -1;
 answer[1] = -1;
 b = 0;
 while (idx[2][queue[front]] != 1) {
 front++;
 }
 if (idx[1][queue[front]] != len){
 if (sol2[0][idx[1][queue[front]]] == one && sol2[1][idx[1][queue[front]]] == 0){
 answer[b++] = sol[idx[1][queue[front]]];
 }
 }
 if (idx[0][queue[front]] != len){
 if (sol2[0][idx[0][queue[front]]] == one && sol2[1][idx[0][queue[front]]] == 0)
 {
 answer[b++] = sol[idx[0][queue[front]]];
 }
 }
 printf("%d ", b);
 if (b > 0){
 printf("%d ", answer[0]);
 if (b == 2)
 printf("%d", answer[1]);
 }
 printf("\n");
 }
 }
 return 0;}
int compare(const void *a, const void *b){
 return *(int *)a - *(int *)b;}
int search(int *arr, int value, int start, int end){
 int mid = (start + value) / 2;
 while (arr[mid] != end){
 mid = (start + value) / 2;
 if (end < arr[mid])
 start = mid - 1;
 if (end > arr[mid])
 value = mid + 1;
 if (value > start)
 return -1;
 }
 return mid;}
