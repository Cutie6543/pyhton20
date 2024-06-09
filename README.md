# pyhton20
a python program on pascals triangle
def generate_pascals_triangle(num_rows):
    if num_rows <= 0:
        return []

    triangle = [[1]]  

    for i in range(1, num_rows):
        row = [1]  
        for j in range(1, i):
         row.append(triangle[i-1][j-1] + triangle[i-1][j])
        row.append(1)  
        triangle.append(row)
        return triangle;
num_rows = 5
triangle = generate_pascals_triangle(num_rows)
for row in triangle:
    print(row)
