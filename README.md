# Arbitrary Precision Calculator 🔢

## 📌 Overview

The APC (Arbitrary Precision Calculator) is a program designed to perform arithmetic operations on large numbers that cannot be handled by standard data types like `int` or `float`. This project allows users to perform addition, subtraction, multiplication, and division of large numbers represented as doubly linked lists.

The program supports various operations including handling both positive and negative numbers, and provides results with precision beyond standard data types.

## 🔧 Features

- **Addition** — Adds two large numbers
- **Subtraction** — Subtracts one large number from another including borrowing
- **Multiplication** — Multiplies two large numbers handling carries and partial products
- **Division** — Divides two large numbers with appropriate error handling

## 🧰 Project Structure

- `addition.c` — Logic for adding two large numbers
- `subtraction.c` — Logic for subtracting two large numbers
- `multiplication.c` — Logic for multiplying two large numbers
- `division.c` — Logic for dividing two large numbers
- `read_valid.c` — Handles reading and validating input from the user
- `apc.h` — Header file declaring necessary functions and data structures

## 🧠 Data Structures

The primary data structure used is a **Doubly Linked List (Dlist)** where each node represents a single digit of a large number.

### `Dlist` Structure
Each node in the doubly linked list stores:
```c
typedef struct Dlist {
    int data;           // A digit of the large number
    struct Dlist *prev; // Pointer to previous node
    struct Dlist *next; // Pointer to next node
} Dlist;
```

### `Slist` Structure
Each node in the singly linked list stores temporary results:
```c
typedef struct Slist {
    int data;           // A digit for temporary results
    struct Slist *link; // Pointer to next node
} Slist;
```

## ⚙️ Functionality

### 1. Addition
- **Function:** `addition()`
- Adds two numbers represented by doubly linked lists and stores result

### 2. Subtraction
- **Function:** `subtraction()`
- Subtracts one large number from another, handling borrowing when necessary

### 3. Multiplication
- **Function:** `multiplication()`
- Multiplies two large numbers, handling carries and partial products

### 4. Division
- **Function:** `division()`
- Divides one large number by another and stores the quotient

### 5. Input and Validation
- **Functions:** `read_input()`, `check_operation_type()`, `read_and_validate_args()`
- Reads, validates input and ensures correct operation is selected

## ⚠️ Error Handling

- **Invalid Operation** — Unsupported operation prints error and terminates
- **Division by Zero** — Displays error message and returns `FAILURE`
- **Invalid Operand** — Non-numeric characters are detected and reported

## 🚀 How to Compile & Run
```bash
# Compile
gcc addition.c subtraction.c multiplication.c division.c read_valid.c -o apc

# Run
./apc
```

## 💡 Example Usage
```bash
# Addition
./apc 12345678901234567890 + 98765432109876543210

# Multiplication
./apc 99999999999999999999 x 99999999999999999999
```

## What I Learned

- Doubly linked list implementation and manipulation in C
- Dynamic memory management and pointer arithmetic
- Handling large number arithmetic beyond standard data types
- Modular programming and file organization in C
- Edge case handling and robust error management

## Author

**Miryala Vamshi**  
Embedded Systems Engineer  
📧 vamshimiryala2@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/vamshi-miryala-a7b71a347)
