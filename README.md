# Python-program-to-implement-Binary-Search
def binarySearch(numbers, low, high, x):
    if high >= low:
        mid = (low + high) // 2

        if numbers[mid] == x:
            return mid
        elif numbers[mid] > x:
            return binarySearch(numbers, low, mid - 1, x)
        else:
            return binarySearch(numbers, mid + 1, high, x)
    else:
        return -1


numbers = [9, 4, 6, 7, 2, 1, 5]
numbers.sort()

x = 7

result = binarySearch(numbers, 0, len(numbers) - 1, x)

if result != -1:
    print("Search successful, element found at position", result)
else:
    print("Search unsuccessful")
    output
Search successful, element found at position 5    
