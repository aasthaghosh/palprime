# palprime
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def is_palindrome(n):
    return str(n) == str(n)[::-1]

def find_palindrome_primes(start, end):
    palprime_numbers = []
    for num in range(start, end + 1):
        if is_prime(num) and is_palindrome(num):
            palprime_numbers.append(num)
    return palprime_numbers

# Input range to find Palindrome Prime numbers
start_range = int(input("Enter the start of the range: "))
end_range = int(input("Enter the end of the range: "))

# Find Palindrome Prime numbers within the specified range
palprime_nums = find_palindrome_primes(start_range, end_range)

if palprime_nums:
    print(f"Palindrome Prime numbers in the range {start_range} to {end_range}: {palprime_nums}")
else:
    print(f"No Palindrome Prime numbers found in the range {start_range} to {end_range}")
