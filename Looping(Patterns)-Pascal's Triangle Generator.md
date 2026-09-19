# 🔺 Looping(Patterns)-Pascal's Triangle Generator in Python

This project demonstrates a simple Python program to generate **Pascal’s Triangle**, where the number of rows is provided by the user.

---

## 🎯 Aim

To write a Python program that generates **Pascal's Triangle** using numbers. The number of rows is accepted from the user.



## 🧠 Algorithm

1. Start the program.
2. Input the number of rows from the user.
3. Loop from 0 to the number of rows.
4. For each row:
   - Print appropriate spaces to shape the triangle.
   - Compute values using the formula:  
     \[
     C(n, k) = \frac{n!}{k!(n-k)!}
     \]
5. Print all rows of Pascal’s Triangle.
6. End the program.

---

## 🧪 Program
`````
def print_pascal_triangle(n: int) -> None:
    for i in range(n):
        for j in range(n - i - 1):
            print(" ", end="")
        for j in range(i + 1):
            print(binomial_coefficient(i, j), end=" ")
        print()

def binomial_coefficient(n: int, k: int) -> int:
    res = 1
    if k > n - k:
        k = n - k
    for i in range(k):
        res *= (n - i)
        res //= (i + 1)
    return res

n = int(input())
print_pascal_triangle(n)


`````

## Sample Output

<img width="735" height="577" alt="image" src="https://github.com/user-attachments/assets/33cc4370-ad9d-4762-9882-681abd55e2aa" />

## Result
Thus, the program has been successfully executed.
