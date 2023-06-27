#!/usr/bin/python3

import sys

def factorize(number):
    factors = []
    for i in range(2, number//2 + 1):
        if number % i == 0:
            factors.append((i, number//i))
    return factors

def main():
    if len(sys.argv) != 2:
        print(f"Usage: factors <filename>")
        return

    filename = sys.argv[1]

    try:
        with open(filename, 'r') as file:
            for line in file:
                number = int(line.strip())
                factor_pairs = factorize(number)
                for pair in factor_pairs:
                    p, q = pair
                    print(f"{number}={p}*{q}")

    except FileNotFoundError:
        print(f"File '{filename}' not found.")

if __name__ == '__main__':
    main()
