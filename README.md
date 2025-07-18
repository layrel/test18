# С помощью цикла создайте матрицу вида 10x10
# Решение:
import random

def generate_matrix(rows, cols):
    return [[random.randint(-20, 20) for _ in range(cols)] for _ in range(rows)]

def add_matrices(matrix1, matrix2):
    rows = len(matrix1)
    cols = len(matrix1[0])
    result = [[0 for _ in range(cols)] for _ in range(rows)]

    for i in range(rows):
        for j in range(cols):
            result[i][j] = matrix1[i][j] + matrix2[i][j]

    return result


rows, cols = 10, 10


matrix_1 = generate_matrix(rows, cols)
matrix_2 = generate_matrix(rows, cols)

print("Первая матрица (matrix_1):")
for row in matrix_1:
    print(row)

print("\nВторая матрица (matrix_2):")
for row in matrix_2:
    print(row)

matrix_3 = add_matrices(matrix_1, matrix_2)

print("\nРезультат сложения (matrix_3):")
for row in matrix_3:
    print(row)
