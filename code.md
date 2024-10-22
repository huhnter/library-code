from functools import reduce

def calculate_stats(numbers):
    # Use map() to square each number
    squares = list(map(lambda x: x ** 2, numbers))
    
    # Use filter() to keep only even numbers
    evens = list(filter(lambda x: x % 2 == 0, numbers))
    
    # Use reduce() to find the product of all numbers
    product = reduce(lambda x, y: x * y, numbers)
    
    # Use zip() to pair numbers with their squares
    pairs = list(zip(numbers, squares))
    
    # Use enumerate() to get index and value
    indexed_numbers = list(enumerate(numbers, start=1))
    
    # Use sorted() to sort numbers in reverse order
    sorted_numbers = sorted(numbers, reverse=True)
    
    # Use any() to check if any number is greater than 50
    has_large_number = any(x > 50 for x in numbers)
    
    # Use all() to check if all numbers are positive
    all_positive = all(x > 0 for x in numbers)
    
    # Print results
    print("Original numbers:", numbers)
    print("Squared numbers:", squares)
    print("Even numbers:", evens)
    print("Product of numbers:", product)
    print("Pairs of numbers and their squares:", pairs)
    print("Indexed numbers:", indexed_numbers)
    print("Sorted numbers (descending):", sorted_numbers)
    print("Any number greater than 50:", has_large_number)
    print("All numbers are positive:", all_positive)

numbers = [5, 10, 15, 20, 25, 30]
calculate_stats(numbers)
