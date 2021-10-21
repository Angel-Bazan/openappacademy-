
# Ruby
## Conditionals 

### Is Div By Five:
Write a method is_div_by_5(number) that takes in a number and returns the boolean true if the given number is divisible by 5, false otherwise

### Syntax:

```jsx
def is_div_by_5(number)
  if number % 5 === 0 
    return true 
  else 
    return false 
  end
end

puts is_div_by_5(10) # => true
puts is_div_by_5(40) # => true
puts is_div_by_5(42) # => false
puts is_div_by_5(8)  # => false 
``` 

### Either Only: 
Write a method either_only(number) that takes in a number and returns true if the number is divisible by either 3 or 5, but not both. The method should return false otherwise. 

### Syntax: 

```jsx 
 def either_only(number)
 if (number % 3 == 0 || number % 5 == 0) && !(number % 3 == 0 && number % 5 == 0)
   return true 
 else 
   return false 
 end
end

puts either_only(9)  # => true
puts either_only(20) # => true
puts either_only(7)  # => false
puts either_only(15) # => false
puts either_only(30) # => false
```

### Larger Number:
Write a method larger_number(num1, num2) that takes in two numbers and returns the larger of the two numbers. 

### Syntax: 

```jsx 
def larger_number(num1, num2)
  if num1 > num2 
    return num1 
  else 
    return num2 
  end
end

puts larger_number(42, 28)   # => 42
puts larger_number(99, 100)  # => 100
``` 
### Longer String: 
Write a method longer_string(str1, str2) that takes in two strings and returns the longer of the two strings. In the case of a tie, the method should return the first string.

### Syntax: 

```jsx 
def longer_string(str1, str2)
 if str1.length >= str2.length # remember about the greater than/ less than or equal sign 
   return str1 
 else 
  return str2 
 end 
end

puts longer_string("app", "academy") # => "academy"
puts longer_string("summer", "fall") # => "summer"
puts longer_string("hello", "world") # => "hello"
```
### Number Check: 
Write a method number_check(num) that takes in a number and returns a string. The method should return the string 'positive' if the num is positive, 'negative' if the num is negative, and 'zero' if the num is zero.

### Syntax: 

```jsx 
def number_check(num)
  if num > 0 
    return 'positive' 
  elsif num < 0 
    return 'negative' 
  else 
    return 'zero' 
  end
end

puts number_check(5)    # => "positive"
puts number_check(-2)   # => "negative"
puts number_check(0)    # => "zero"


```
### Word Check: 
Write a method word_check(word) that takes in a word and returns a string. The method should return the string "long" if the word is longer than 6 characters, "short" if it is less than 6 characters, and "medium" if it is exactly 6 characters long. 

```jsx 
def word_check(word)
  if word.length > 6 
    return "long" 
  elsif word.length < 6 
    return "short" 
  else 
    return "medium"
  end
end

puts word_check("contraption") # => "long"
puts word_check("fruit")       # => "short"
puts word_check("puzzle")      # => "medium"
```

## Loops 

### Count E 
Write a method count_e(word) that takes in a string word and returns the number of e's in the word

```jsx 
def count_e(word)
  count = 0  /// counting the number of e's starting at 0 with the variable count 
  
  i = 0 /// counting the index of the letter word starting at 0 
  
  while i < word.length 
    char = word[i] /// while loop to go through every index letter of the given word until the word ends 
    
  if char == "e"  /// if statement to go count each 'e' and count them 
    count += 1 
  end 
    
  i += 1 /// going through every index 
  end 
  return count
end

puts count_e("movie") # => 1
puts count_e("excellent") # => 3
```

### Count A 
Write a method count_a(word) that takes in a string word and returns the number of a's in the word. The method should count both lowercase (a) and uppercase (A)

```jsx 
def count_a(word)
  count = 0 
  
  i = 0 
  
 while i < word.length 
   char = word[i] 
   
 if char == 'a' || char == 'A' 
    count += 1 
 end 
   i += 1 
 end 
  return count 
end

puts count_a("application")  # => 2
puts count_a("bike")         # => 0
puts count_a("Arthur")       # => 1
puts count_a("Aardvark")     # => 3
```

### Sum Nums 
Write a method sum_nums(max) that takes in a number max and returns the sum of all numbers from 1 up to and including max. 

```jsx 
def sum_nums(max)
 sum = 0 # adding numbers 
 
  i = 1 # starting the addition with one 
  
  while i <= max # while loop to put a stopping point 
    sum += i # adding the starting with each i 
    
    i += 1 # iteration until reach max 
  end 
  
  return sum # returning the sum 
end

puts sum_nums(4) # => 10, because 1 + 2 + 3 + 4 = 10
puts sum_nums(5) # => 15
```
### Factorial 
Write a method factorial(num) that takes in a number num and returns the product of all numbers from 1 up to and including num.

```jsx 
def factorial(num)
  product = 1 
  
  i = 1 
  while i <= num 
    product *= i 
    
    i += 1 
  end
  
  return product 
end

puts factorial(3) # => 6, because 1 * 2 * 3 = 6
puts factorial(5) # => 120, because 1 * 2 * 3 * 4 * 5 = 120
```
