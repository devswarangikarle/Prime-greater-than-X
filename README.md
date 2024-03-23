# Prime-greater-than-X
Find the minimum prime number greater than or equal to X. Input The only line of the input contains a single integer X  Constraints: 2 ≤ X ≤ 105 Output Print the answer

def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

def next_prime(x):
    while True:
        if is_prime(x):
            return x
        x += 1

x = int(input().strip())

print(next_prime(x))
