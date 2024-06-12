# Bootcamp Assignment: Calculate Run Time.

This is a solution to the bootcamp assignment no.3, Run time calculation.

- 1- This code computes the product of two variables, what is the runtime of
  this code?

  ```
  int product(int a, int b) {
  int sum = 0;
  for (int i = 0; i < b; i++) {
    sum += a;
  }
  return sum;
  }
  ```

  Solution:
  The run time for this code will be **_O(n)_** Linear time complexity.
  cause as the input increase in size (which is b), so does the number of operations.

- 2- This code computes A ^ B, what would be the runtime?

  ```
  static int power(int a, int b) {
  if (b < 0) return a;
  if (b == 0) return 1;
  int sum = a;
  for (int I = 0; I < b - 1; I++) {
  sum *= a;
  }
  return sum;
  }

  ```

  Solution:
  The run time for this question is also **_O(n)_**, Linear time,
  because it is concerned with input of **b**.

- 3- This code computes A% B, what would be the runtime?

  ```
  int mod(int a, int b) {
  if (b <=a) return -1;
  int div = a / b;
  return a - div * b;
  }
  ```

  Solution:
  The run time will be Constant **_O(1)_** because all operations are happening in
  constant time, with no loops, or recursive calls.

- 4- This code computes a division between whole integers (assuming both
  are positive), what would be the runtime?

  ```
  int div(int a, int b) {
  int count = a;
  int sum = b;
  while (sum <= a) {
    sum += b;
    count++;
  }
  return count;
  }
  ```

  Solution:
  Because the sum increases be _b_ times in each loop, the run time
  will be **O(a/b)** because it gonna run be _a_ divided be _b_ times.

- 5-
- 6-

- 7- If a binary search tree (BST) is not balanced, how long could it take in
  the worst case to find an item?
  Solution:
  If the BST is not balanced, the worst case gonna be **O(n)**, because
  it's gonna iterate over all the items in the tree, because the item we
  are looking for may be in the far right or far left.

- 8- What would be the worst case if we are looking for a value in a binary
  tree (Binary Tree - BT) that is not ordered?
  Solution:
  Because the tree is not ordered, in the worst case
  you must visit each node in the tree, which means a
  run time of **O(n)**.

- 9- The appendToNew method adds a value to an array by creating a new,
  longer array and returning this longer array. How long does it take to
  copy the array?

  ```
  int[] copyArray(int[] array) {
  int[] copy = new int[0];
  for (int value : array) {
  copy = appendToNew(copy, value);
  }
  return copy;
  }
  int[] appendToNew(int[] array, int value) {
  int[] bigger = new int[array.length + 1];
  for (int I = 0; I < array. length; I++) {
  bigger[I] = array[I];
  }
  bigger[bigger.length - 1] = value;
  return bigger;
  }
  ```

  Solution:
  Because copyArray has a loop that will call appendToNew function
  for each value in the array, and the appendToNew also has a loop
  that copy each element into a new larger array, so the answer is
  $O(n^2)$, because it's nested loop.

- 10- The following code adds the digits of a number. What is your runtime?

  ```
  int sumDigits(int n) {
  int sum = 0;
  while (n > 0) {
  sum += n % 10;
  n /= 10;
  }
  return sum;
  }
  ```
  Solution:
  The run time for this method will be $O(log n)$, because
  the while loop will run until n reaches 0, n is divided by
  10 with each iteration, so it's $O(log_{10} n)$ but bases in
  Big-O notations are ignored.

