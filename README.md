
# Ruby
## Conditionals 

### Description:
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

### Description 
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

