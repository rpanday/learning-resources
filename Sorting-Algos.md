### Comparison-based Sorting Algorithms:
- BUB - Bubble Sort,
```
//O(N^2)
void bubbleSort(int a[], int N) {
   for(int i=0; i<N; i++){
       for(int j=i; j<N; j++){
           if(a[j] < a[i])
               swap(a[i], a[j]);
       }
   }
}
```
- SEL - Selection Sort,
```
//O(N^2)
void selectionSort(int a[], int N) {
  for (int L = 0; L <= N-2; L++) { // O(N)
    int X = min_element(a+L, a+N) - a; // O(N)
    swap(a[X], a[L]); // O(1), X may be equal to L (no actual swap)
  }
}
```
- INS - Insertion Sort,
```
//O(N^2)
void insertionSort(int a[], int N) {
  for (int i = 1; i < N; i++) { // O(N)
    X = a[i]; // X is the item to be inserted
    int j = i-1;
    for (; j >= 0 && a[j] > X; j--) // can be fast or slow
      a[j+1] = a[j]; // make a place for X
    a[j+1] = X; // index j+1 is the insertion point
  }
}
```
- MER - Merge Sort (recursive implementation),
- QUI - Quick Sort (recursive implementation),
- R-Q - Random Quick Sort (recursive implementation).
### Not Comparison-based Sorting Algorithms:
- COU - Counting Sort,
- RAD - Radix Sort.

source: https://visualgo.net/en/sorting?slide=4-1
