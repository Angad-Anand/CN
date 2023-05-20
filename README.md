# CN
<!-- Write a Python program to rescale and shift numbers in a given list, so that they cover the range -->
def test(nums):
    a = min(nums)
    b = max(nums)
    if b - a == 0:
        return [0.0] + [1.0] * (len(nums) - 1)
    for i in range(len(nums)):
        nums[i] = (nums[i] - a) / (b - a)
    return nums

nums = [18.5, 17.0, 18.0, 19.0, 18.0]
print("Original list:")
print(nums)
print("Rescale and shift the numbers of the said list so that they cover the range [0, 1]:")
print(test(nums))

<!--  Write a Python program to reverse the case of all strings. For those strings, which contain no
letters, reverse the strings. -->
def test(strs: list[str]) -> list[str]:
  return [s.swapcase() if any(c.isalpha() for c in s) else s[::-1] for s in strs]
strs = ['cat', 'catatatatctsa', 'abcdefhijklmnop', '124259239185125', '', 'foo', 'unique']
print("Original list:")
print(strs)
print("Reverse the case of all strings. For those strings which contain no letters, reverse the strings:")
print(test(strs))

<!-- Write a Python program to compute the product of the odd digits in a given number, or 0 if there aren't any. -->
def test(n):
    if any(int(c) % 2 for c in str(n)):
        prod = 1
        for c in str(n):
            if int(c) % 2 == 1:
                prod *= int(c)
        return prod
    return 0

n = 123456789
print("Original Number:",n)
print("Product of the odd digits in the said number, or 0 if there aren't any")
print(test(n))
n = 2468
print("\nOriginal Number:",n)
print("Product of the odd digits in the said number, or 0 if there aren't any")
print(test(n))

<!-- Write a Python function that accepts a string and counts the number of upper and lower case letters. -->
def string_test(s):
    d={"UPPER_CASE":0, "LOWER_CASE":0}
    for c in s:
        if c.isupper():
           d["UPPER_CASE"]+=1
        elif c.islower():
           d["LOWER_CASE"]+=1
        else:
           pass
    print ("Original String : ", s)
    print ("No. of Upper case characters : ", d["UPPER_CASE"])
    print ("No. of Lower case Characters : ", d["LOWER_CASE"])
string_test('The quick Brown Fox')

<!-- Write a Python program to find an integer exponent x such that a^x = n -->
def test(n,a):
    m = 1
    x = 0
    while m != n:
        x += 1
        m *= a
    return x
a = 2
n = 1024
print("a = ",a,": n = ",n)
print("Find an integer exponent x such that a^x = n:")    
print(test(n,a))

<!-- Write a Python program to compute the sum of the ASCII values of the upper-case charactersn in a given string. -->
def test(strs):
    return sum(map(ord,filter(str.isupper,strs)))
strs =  "JavaScript"
print("\nOriginal strings:")
print(strs)
print("Sum of the ASCII values of the upper-case characters in the said string:")
print(test(strs))


