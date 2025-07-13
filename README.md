# Python-programming
def merapahaadhh(limit):
    multiples = [7, 11, 13, 17]
    num_list = []
    i = 1
    while True:
        num = multiples[(i - 1) % len(multiples)] * i
        if num > limit:
            break
        num_list.append(num)
        i += 1
    rows = 1
    total_numbers = 0
    while total_numbers + rows <= len(num_list):
        total_numbers += rows
        rows += 1
    count = 0
    for i in range(1, rows):
        print(" " * (rows - i), end="")  
        for j in range(i):
            if count < len(num_list):
                print(num_list[count], end=" ")
                count += 1
        print()
limit = 5000
merapahaadhh(limit)

