# binary-search-tree-validator
# Binary Search Tree Validator in C

This project implements a C program to verify if a given binary tree is a Binary Search Tree (BST). The program includes functions to create nodes, insert nodes into a BST, and check if a tree satisfies BST properties. It also performs an in-order traversal to display the tree structure.

## Features

- **Node Creation**: Functions to create nodes for both standard and binary search trees.
- **Insertion**: Insert nodes into a binary search tree while maintaining BST properties.
- **BST Validation**: Check if a given tree is a BST using a recursive algorithm.
- **In-Order Traversal**: Display the tree structure using an in-order traversal.

## Data Structures

### `Nodo`
The `Nodo` structure represents a node in the binary tree:
- `valor`: Integer value stored in the node.
- `esq`: Pointer to the left child node.
- `dir`: Pointer to the right child node.

## Functions

### `Nodo* criaNodoABB(int valor)`
Creates a new node with the specified value and initializes its left and right children to `NULL`.

### `Nodo* criaNodo(int valor, Nodo* noEsq, Nodo* noDir)`
Creates a new node with the specified value, left child, and right child.

### `Nodo* insereABB(Nodo* p, int x)`
Inserts a new value into the binary search tree. Returns the root of the updated tree.

### `int ehABB(Nodo* nodo, int direcao, int num)`
Checks if a given tree is a binary search tree (BST). Returns `1` if true, `0` otherwise.

### `void exibe_simetrica(Nodo* p)`
Displays the tree structure in an in-order traversal.

## Compilation and Execution

To compile and run the program, follow these steps:

1. **Compile the code**:
   ``` gcc -o bst_validator main.c ```

2. **Run the program**:
   ``` ./bst_validator ```

## Example

The program constructs and validates two example trees.

### Example 1:
- Tree Construction:
  ```
  raiz = insereABB(raiz, 10);
  insereABB(raiz, 5);
  insereABB(raiz, 15);
  insereABB(raiz, 3);
  insereABB(raiz, 7);
  ```

- Output:
  ``` 
  Arvore em ordem simetrica: 
  ptr_no=0x... chave=3 esq=0x0 dir=0x0
  ptr_no=0x... chave=5 esq=0x0 dir=0x...
  ptr_no=0x... chave=7 esq=0x0 dir=0x0
  ptr_no=0x... chave=10 esq=0x... dir=0x...
  ptr_no=0x... chave=15 esq=0x0 dir=0x0
  ```

- Validation:
  ``` 
  Esta e uma arvore ABB
  ```

### Example 2:
- Tree Construction:
  ```
  Nodo* n20 = criaNodo(20, NULL, NULL);
  Nodo* n60 = criaNodo(60, NULL, NULL);
  Nodo* n80 = criaNodo(80, NULL, n20);
  Nodo* n70 = criaNodo(70, n60, n80);
  Nodo* n40 = criaNodo(40, NULL, NULL);
  Nodo* n30 = criaNodo(30, NULL, n40);
  Nodo* n50 = criaNodo(50, n30, n70);
  raiz2 = n50;
  ```

- Output:
  ``` 
  Arvore 2 em ordem simetrica: 
  ptr_no=0x... chave=30 esq=0x0 dir=0x...
  ptr_no=0x... chave=40 esq=0x0 dir=0x0
  ptr_no=0x... chave=50 esq=0x... dir=0x...
  ptr_no=0x... chave=60 esq=0x0 dir=0x0
  ptr_no=0x... chave=70 esq=0x... dir=0x...
  ptr_no=0x... chave=80 esq=0x0 dir=0x...
  ptr_no=0x... chave=20 esq=0x0 dir=0x0
  ```

- Validation:
  ``` 
  Esta e uma arvore ABB
  ```
