
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

## Reverse 
Write a method reverse(word) that takes in a string word and returns the word with its letters in reverse order.

```jsx 
def reverse(word)
  rev = "" 
  i = 0 
  
  while i < word.length 
    char = word[i] 
    rev = char + rev // by inputting the char first in the addition it adds the index character in front making the word reverse 
    
    i += 1 
    
  end 
  return rev 
end

puts reverse("cat")          # => "tac"
puts reverse("programming")  # => "gnimmargorp"
puts reverse("bootcamp")     # => "pmactoob"
```
## Doubler 
Write a method doubler(numbers) that takes an array of numbers and returns a new array
where every element of the original array is multiplied by 2.

```jsx 
def doubler(numbers)
  double_num = [] ///creating a new array 
  
  i = 0 ///starting at index 0 
  while i < numbers.length ///stopping at the last index
   
    double_num << numbers[i] * 2
    
    i +=1
  end
  
return double_num
end

print doubler([1, 2, 3, 4]) # => [2, 4, 6, 8]
puts
print doubler([7, 1, 8])    # => [14, 2, 16]
```
## Yell
Write a method yell(words) that takes in an array of words and returns a
new array where every word from the original array has an exclamation point after it.

```jsx 
def yell(words)
 scream = [] //creating new array 
  
  i = 0 
   while i < words.length 
     word = words[i] // creating a new variable for every index from words 
     scream_word = word + '!' //creating a new variable that has the addition of that word plus the exclamation point 
     scream << scream_word ///shoveling that new variable into the new array 
     
     i += 1 //iterating to every single array 
   end
  return scream /// return the new array 
end

print yell(["hello", "world"]) # => ["hello!", "world!"]
puts
print yell(["code", "is", "cool"]) # => ["code!", "is!", "cool!"]
```
## Even 
Write a method even_nums(max) that takes in a number max and returns an array containing all even numbers from 0 to max

```jsx 
def even_nums(max)
 evens = []
i = 0 
  
  while i <= max 
    if i % 2 === 0 
      evens << i 
    end 
    
  i+=1 
  end 
   return evens 
end 
print even_nums(10) # => [0, 2, 4, 6, 8, 10]
puts
print even_nums(5)  # => [0, 2, 4]
```

## Range 
Write a method range(min, max) that takes in two numbers min and max. The method should return an array containing all numbers from min to max inclusive.

```jsx 
def range(min, max)
  list = []
  i = min 
  
  while i <= max 
    list << i 
  
    
    i+=1
  end 
  return list 
end

print range(2, 7)   # => [2, 3, 4, 5, 6, 7]
puts
print range(13, 20) # => [13, 14, 15, 16, 17, 18, 19, 20]
```
## Odd Range 
Write a method odd_range(min, max) that takes in two numbers min and max. The method should return an array containing all odd numbers from min to max (inclusive).

```jsx 
def odd_range(min, max)
 odd = []
  i = min 
  
  while i <= max 
    if i % 2 != 0 
      odd << i 
    end 
    i += 1 
  end 
  return odd
end

print odd_range(11, 18) # => [11, 13, 15, 17]
puts
print odd_range(3, 7)   # => [3, 5, 7]
```
## Reverse Range 
Write a method reverse_range(min, max) that takes in two numbers min and max. The function should return an array containing all numbers from min to max in reverse order. The min and max should be excluded from the array

```jsx
def reverse_range(min, max)
reverse = []
  i = max -1
  
  while i > min

     reverse << i 
    i-=1 
  end 
  return reverse
end

print reverse_range(10, 17) # => [16, 15, 14, 13, 12, 11]
puts
print reverse_range(1, 7)   # => [6, 5, 4, 3, 2]
```
## First Half 
Write a method first_half(array) that takes in an array and returns a new array containing the first half of the elements in the array. If there is an odd number of elements, return the first half including the middle element.

```jsx 
def first_half(array)
 half = [] 
  i = 0 
  
  while i < (array.length / 2.0)
  ele = array[i] 
    half << ele 
    
  i+=1 
  end 
  return half 
end

print first_half(["Brian", "Abby", "David", "Ommi"]) # => ["Brian", "Abby"]
puts
print first_half(["a", "b", "c", "d", "e"])          # => ["a", "b", "c"]
```

## Factors Of 
Write a method factors_of(num) that takes in a num and returns an array of all positive numbers less than or equal to num that can divide num.
 
 
 ```jsx 
 def factors_of(num)
 factors = [] 
  i = 1 
  while i <= num 
    if num % i === 0 
      factors << i 
    end 
  i+=1 
  end 
  return factors 
end
print factors_of(3)   # => [1, 3]
puts
print factors_of(4)   # => [1, 2, 4]
puts
print factors_of(8)   # => [1, 2, 4, 8]
puts
print factors_of(9)   # => [1, 3, 9]
puts
print factors_of(16)  # => [1, 2, 4, 8, 16]
```

## Select Odds 
Write a method select_odds(numbers) that takes in an array of numbers and returns a new array containing the odd numbers of the original array.

```jsx
def select_odds(numbers)
  odds = [] 
  i = 0 
  
  while i < numbers.length
    num = numbers[i] 
    
    if num % 2 === 1 
      odds << num 
    end 
    i+=1 
  end 
  return odds
end

print select_odds([13, 4, 3, 7, 6, 11]) # => [13, 3, 7, 11]
puts
print select_odds([2, 4, 6])            # => []
```

## Select Long Words
Write a method select_long_words(words) that takes in an array of words and returns a new array containing all of the words of the original array that are longer than 4 characters.

```jsx 
def select_long_words(words)
  long = [] 
  i = 0 
  
  while i < words.length 
    word = words[i] 
    if word.length > 4 
       long << word 
    end 
    i+=1 
  end 
  return long 
end

print select_long_words(["what", "are", "we", "eating", "for", "dinner"]) # => ["eating", "dinner"]
puts
print select_long_words(["keep", "coding"])                               # => ["coding"]
```

## Sum Elements
Write a method sum_elements(arr1, arr2) that takes in two arrays. The method should return a new array containing the results of adding together corresponding elements of the original arrays. You can assume the arrays have the same length.

```jsx 
def sum_elements(arr1, arr2)
  sums = [] 
  i = 0 
  
  while i < arr1.length 
    newArr = arr1[i] + arr2[i] 
    
end

print sum_elements([7, 4, 4], [3, 2, 11])                            # => [10, 6, 15]
puts
print sum_elements(["cat", "pizza", "boot"], ["dog", "pie", "camp"]) # => ["catdog", "pizzapie", "bootcamp"]
```
## Fizz Buzz
Write a method fizz_buzz(max) that takes in a number max and returns an array containing all numbers greater than 0 and less than max that are divisible by either 4 or 6, but not both.

```jsx 
def fizz_buzz(max)
 newArr = []
  i = 0 
  
  while  i < max 
    if (i % 4 === 0 || i % 6 === 0) && !(i % 4 === 0 && i % 6 === 0 ) 
      newArr << i
    end 
    i+=1 
  end 
  return newArr
end

print fizz_buzz(20) # => [4, 6, 8, 16, 18]
puts
print fizz_buzz(15) # => [4, 6, 8]
```

## To Initials
Write a method to_initials that takes in a person's name string and returns a string representing their initials.

```jsx 
def to_initials(name)
names = name.split(" ") 
initials = " " 
names.each { |n| initials += n[0] }
return initials 

end

puts to_initials("Kelvin Bridges")      # => "KB"
puts to_initials("Michaela Yamamoto")   # => "MY"
puts to_initials("Mary La Grange")      # => "MLG"
```

## First In Array
Write a method first_in_array that takes in an array and two elements, the method should return the element that appears earlier in the array.

```jsx
def first_in_array(arr, el1, el2)
    if arr.index(el1) < arr.index(el2)
      return el1
    else 
      return el2
  end 
end

puts first_in_array(["a", "b", "c", "d"], "d", "b"); # => "b"
puts first_in_array(["cat", "bird" ,"dog", "mouse" ], "dog", "mouse"); # => "dog"
```
## Abbreviate Sentence 
Write a method abbreviate_sentence that takes in a sentence string and returns a new sentence where every word longer than 4 characters has all of it's vowels removed.

```jsx
def abbreviate_sentence(sent)
 words = sent.split(" ") 
 new_words = [] 
  
  words.each do |word| 
    if word.length > 4 
      new_word = abbreviate_word(word) 
      new_words << new_word 
     else 
       new_words << word
     end 
  end 
  return new_words.join(" ") 
end

def abbreviate_word(word)
  vowels = "aeiou"
  no_vowels = ""
  
  word.each_char do |char| 
    if !vowels.include?(char)
      no_vowels += char 
    end  
  end
   return no_vowels 
end

puts abbreviate_sentence("follow the yellow brick road") # => "fllw the yllw brck road"
puts abbreviate_sentence("what a wonderful life")        # => "what a wndrfl life"
```


## Format Name
Write a method format_name that takes in a name string and returns the name properly capitalized. 

```jsx 
# Hint: use str.upcase and str.downcase
# "abc".upcase # => "ABC"

def format_name(str)
  parts = str.split(' ')
  new_parts = []
  
  parts.each do |part|
    
    new_parts << part[0].upcase + part[1..-1].downcase 
  end 
  
  return new_parts.join(' ')
end

puts format_name("chase WILSON") # => "Chase Wilson"
puts format_name("brian CrAwFoRd scoTT") # => "Brian Crawford Scott"
```

## Is Valid Name
Write a method is_valid_name that takes in a string and returns a boolean indicating whether or not it is a valid name.

```jsx 
# A name is valid is if satisfies all of the following:
# - contains at least a first name and last name, separated by spaces
# - each part of the name should be capitalized
#
# Hint: use str.upcase or str.downcase
# "a".upcase # => "A"

def is_valid_name(str)
  parts = str.split(" ") 
    if parts.length < 2
      return false 
    end 
   
  parts.each do |part|
    if is_capitalized(part) 
      return true
    end
  end
  return false
end
  
  def is_capitalized(word) 
    if word[0] == word[0].upcase && word[1..-1] == word[1..-1].downcase 
      return true 
    else 
      return false 
    end 
  end


puts is_valid_name("Kush Patel")       # => true
puts is_valid_name("Daniel")           # => false
puts is_valid_name("Robert Downey Jr") # => true
puts is_valid_name("ROBERT DOWNEY JR") # => false
```

## Is Valid Email 
Write a method is_valid_email that takes in a string and returns a boolean indicating whether or not it is a valid email address. 

```jsx 
# For simplicity, we'll consider an email valid when it satisfies all of the following:
# - contains exactly one @ symbol
# - contains only lowercase alphabetic letters before the @
# - contains exactly one . after the @

def is_valid_email(str)
 parts = str.split("@") 
  if parts.length != 2 
    return false 
  end 
  
  first = part[0] 
  sencond = part[1] 
  words = "abcdefghijklmnopqrstuvwxyz"
  
  first.each_char do |char|
    !words.include?(char)
     return false
    end
 end
   
  if second.split(".").length == 2 
    return true 
  else 
    return false 
  end 
end 
  
  
end

puts is_valid_email("abc@xy.z")         # => true
puts is_valid_email("jdoe@gmail.com")   # => true
puts is_valid_email("jdoe@g@mail.com")  # => false
puts is_valid_email("jdoe42@gmail.com") # => false
puts is_valid_email("jdoegmail.com")    # => false
puts is_valid_email("az@email")         # => false
```

## Reverse Words
Write a method reverse_words that takes in a sentence string and returns the sentence with the order of the characters in each word reversed. Note that we need to reverse the order of characters in the words, do not reverse the order of words in the sentence.

```jsx 
def reverse_words(sent)
  parts = sent.split(" ")
  new_arr = [] 
  
  parts.each { |word| new_arr << word.reverse } 
  new_sent = new_arr.join(" ") 
  
  return new_sent
      
end

puts reverse_words('keep coding') # => 'peek gnidoc'
puts reverse_words('simplicity is prerequisite for reliability') # => 'yticilpmis si etisiuqererp rof ytilibailer'
```
