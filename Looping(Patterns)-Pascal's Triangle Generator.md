# 🔺 Looping(Patterns)-Pascal's Triangle Generator in Python

This project demonstrates a simple Python program to generate **Pascal’s Triangle**, where the number of rows is provided by the user.

---

## 🎯 Aim

To write a Python program that generates **Pascal's Triangle** using numbers. The number of rows is accepted from the user.

---

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
Add Code Here
```
def generate_pascals_triangle(n):
    triangle = [[1] * (i + 1) for i in range(n)]
    
    for i in range(2, n):
        for j in range(1, i):
            triangle[i][j] = triangle[i - 1][j - 1] + triangle[i - 1][j]
    
    return triangle

def print_pascals_triangle(n):
    triangle = generate_pascals_triangle(n)
    
    for row in triangle:
        print(" ".join(map(str, row)))

rows = int(input())
print_pascals_triangle(rows)
```
## Sample Output
![Screenshot 2025-04-29 102511](https://github.com/user-attachments/assets/e4ec07e9-7394-4aa4-b17d-ce69d2949fc9)

## Result
Thus, the python program was executed successfully
