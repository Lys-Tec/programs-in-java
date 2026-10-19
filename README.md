## Programs in Java

A collection of Java programs I wrote while studying **Data Structures and Algorithms (ICT202)** at Mulungushi University. Each program is a console application that runs in the terminal and shows how a core data structure or technique works in practice.

## Programs

| Program | What it does | Concepts used |
|---|---|---|
| [Towers of Hanoi](#1-towers-of-hanoi) | Solves the Towers of Hanoi puzzle for any number of disks and prints every move | Stacks, recursion |
| [Matrix Operations](#2-matrix-operations) | Menu-driven program that adds, subtracts and multiplies matrices | 2D arrays, loops, exception handling |

---

## 1. Towers of Hanoi

**File:** `TowersOfHanoi.java`

Solves the classic Towers of Hanoi puzzle. The user enters the number of disks, and the program prints the full sequence of moves needed to move all disks from peg **A** to peg **C**, using peg **B** as the helper.

### How it works
- The three pegs are represented by three `Stack<Integer>` objects (source, auxiliary and destination).
- The disks are loaded onto the source stack, with the largest disk at the bottom.
- A recursive method `solve()` moves `n - 1` disks out of the way, moves the largest disk, then moves the `n - 1` disks on top of it.
- Every move is popped from one stack, pushed onto another, and printed.

### Sample output
```
Enter number of disks: 3

Sequence of Moves:
Move disk 1 from A to C
Move disk 2 from A to B
Move disk 1 from C to B
Move disk 3 from A to C
Move disk 1 from B to A
Move disk 2 from B to C
Move disk 1 from A to C
```
A puzzle with `n` disks takes `2^n - 1` moves, so 3 disks gives 7 moves.

---

## 2. Matrix Operations

**File:** `MatrixOperations.java`

A menu-driven program that performs basic matrix operations using 2D arrays.

### Features
1. **Addition** (A + B)
2. **Subtraction** (A - B)
3. **Multiplication** (A x B), with a check that the columns of A equal the rows of B
4. **Display** a matrix
5. **Exit**

The program also handles wrong input, such as typing letters where a number is expected, without crashing. Matrix sizes are limited to between 2x2 and 5x5.

### How it works
- `getSize()` asks for the number of rows or columns.
- `inputMatrix()` reads each element one by one and re-asks if the input is not an integer.
- `displayMatrix()` prints the matrix in rows.
- `addition()`, `subtraction()` and `multiplication()` do the calculations with nested loops.

### Sample output
```
MATRIX OPERATIONS
1. Addition
2. Subtraction
3. Multiplication
4. Display Matrix
5. Exit
Select Operation:
1
Enter rows for matrices: 2
Enter columns for matrices: 2

Enter values for Matrix A
Element [0][0]: 1
Element [0][1]: 2
Element [1][0]: 3
Element [1][1]: 4

Enter values for Matrix B
Element [0][0]: 5
Element [0][1]: 6
Element [1][0]: 7
Element [1][1]: 8

Result (A + B):
| 6 8 |
| 10 12 |
```

---

## How to Run

You need the **Java JDK 8 or higher** installed. Check with:
```
java -version
```

1. Clone the repository:
   ```
   git clone https://github.com/Lys-Tec/programs-in-java.git
   cd programs-in-java
   ```
2. Compile a program:
   ```
   javac TowersOfHanoi.java
   ```
3. Run it:
   ```
   java TowersOfHanoi
   ```
Do the same for `MatrixOperations`. You can also open the folder in **Visual Studio Code** (with the Java extension) and click **Run**.

## What I Learned

- Using the `Stack` class and recursion together to solve a problem
- Working with 2D arrays and nested loops
- Handling bad user input with `try/catch` and `InputMismatchException`
- Breaking a program into small, reusable methods

- Other java programs are for practice purposes


## Author

**Houghton Chibozyi**

BSc Computer Science, Mulungushi University

GitHub: [Lys-Tec](https://github.com/Lys-Tec)**

Email: chibozyih@mail.com 

GitHub: github.com/your-username LinkedIn: linkedin.com/in/your-name/Houghton Chibozyi
