
### Ruby Quiz Questions 

1.How will you extract the inner array value 8?

```ruby
a = [[4, [5, 8]]]

```

Answer :

```ruby
a.dig(0, 1, 1)

```
2. Which method will merge elements of curremt array with corresponding elements from each argument.(index wise)

Answer :

Zip method

```ruby
a = [ 4, 5, 6 ]
b = [ 7, 8, 9 ]



[1, 2, 3].zip(a, b) #=> [[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```
3. How will you make a new copy of a current hash?

Answer :

```ruby
h.clone
```

4. Which method rebuilds the hash based on the current hash values for each key. If values of key objects have changed since they were inserted?

Answer :

rehash method will reindex hash.

```ruby
a = [ "a", "b" ]
c = [ "c", "d" ]

h = { a => 100, c => 300 }

h[a] #=> 100
a[0] = "z"
h[a] #=> nil
h.rehash #=> {["z", "b"]=>100, ["c", "d"]=>300}
h[a] #=> 100
```
5. differentiate - "hex' and "oct" methods in String

Answer :

```ruby
hex - Treats leading characters from str as a string of hexadecimal digits

"0x0a".hex #=> 10
"-1234".hex #=> -4660

oct-Treats leading characters of str as a string of octal digits


"123".oct #=> 83
"-377".oct #=> -255
```
6. Which method is used to check if the string is invalid byte sequence then replace invalid bytes with given replacement character,

Answer :

```ruby
scrub method
"abc\u3042\x81".scrub("*") #=> "abc\u3042*"
```


7. Is everything in Ruby an object?

Answer :

Methods are not objects. Blocks are not objects. Keywords are not objects. However, there exist Method objects and Proc objects, and some keywords refer to objects.


8. What are the subclasses of numeric datatype?

Answer :

Integer,Float,BigDecimal,Complex,Rational


9. If a symbol (say :Friend) is a constant in one context, a method in another, and a class in a third, that :ruby will be the same object in all three contexts. True or false?

Answer :

```ruby
module One
  class Friend
  end
  $f1 = :Friend
end

module Two
  Fred = 1
  $f2 = :Friend
end

def Friend()

end

$f3 = :Friend

$f1.object_id #=> 2514190
$f2.object_id #=> 2514190
$f3.object_id #=> 2514190

```

10. What does "cycle" method will do in an array?

Answer :

```ruby
a.cycle {|x| puts x} # print, a, b, c, a, b, c,.. forever.
```


11. How can you do chain push in an array?

Answer :

```ruby
a = []
a << 1 << 2 << 3
```


12. What are the mehods to check hash keys?

Answer :

Hash#has_key?, Hash#include?, Hash#member?



13. Is ther any class in the name

"Boolean" ? What are the classes that support boolean data type?

Answer :

No,True class, flase class



14. What "quo" method will do in Rational?

Answer :

It will perform division

```ruby
Rational(900)   / Rational(1)      #=> (900/1)
```

15. Explain pred and succ methods in Numeric?

Answer :

```ruby
n.pred will print preceeder
6.pred #5

n.succ will print successor
9.succ #10
```
16. How to display the inbetween values in a range?

Answer :

entries, to_a

17. difference between last and max methods in Range?

Answer :

```ruby
1..10.last= "10"

1...10.max = "9"
```

18. What each_pair method will do? Which class it belongs to?

take the pair values from a hash. Hash class

Answer :

```ruby
h = {foo: 0, bar: 1, baz: 2}
h.each_pair {|key, value| puts "#{key}: #{value}"} # => {:foo=>0, :bar=>1, :baz=>2}
```

19. Can case statement be assigned to any variable?

Answer :

yes. This value can be assigned to a variable preceding the case statement.

```ruby
happy = case

when ...

end

puts happy
```


20. How can you resolve name conflict(same name in mixin modules) in modules?

Answer :

alias_method.

```ruby
module Happy
  def expression
    return "smiling"
  end
 alias happyexpression expression
end

```

21.for this code, which one is true?

```ruby
class ABC
  def xyz
    puts "xyz in ABC"
  end
end. 


1.ABC::new::xyz
2.ABC::new.xyz
3.ABC.new::xyz
4.ABC.new.xyz
```

Answer :

all are true

output "xyz in ABC"


22. Is the below Ruby code valid?

```ruby
-> (a) {p a}["Hello world"]
```

If so, what does it do? Explain your answer.

Answer :

The -> operator creates a new Proc, which is one of Ruby’s function types. (The -> is often called the “stabby proc”.)

This particular Proc takes one parameter (namely, a). When the Proc is called, Ruby executes the block

puts a

23. Which one is true?

```ruby
my_lambda = -> { puts "Lambda called" }

a)my_lambda.call
b)my_lambda.()
c)my_lambda[]
d)my_lambda.===
```
Answer :

All are true.

```ruby
a)my_lambda.call
b)my_lambda.()
c)my_lambda[]
d)my_lambda.===

```
These methods are used to call the lambda


24. Which of the following is true?

defining a regular expression:
```ruby
a)Regexp.new( ‘string pattern' [, options ] )
b)/string pattern/
c)%r{string pattern}
d)->(x){string pattern}

```
Answer :

First three syntax are true.

a)Regexp.new( ‘string pattern' [, options ] )
b)/string pattern/
c)%r{string pattern}

d)->(x){string pattern}

fourth one is lambda syntax

25. What are the meaning of the following character ranges in Regular Expression?

\w
\d
\s

Answer :

```ruby
\w is equivalent to [0-9a-zA-Z_]

\d is the same as [0-9]

\s matches white space (tabs, regular space, newline)

```

26. What are the meaning of the following character ranges in Regular Expression?

\W
\D
\S

Answer :

```ruby
\W anything that’s not in [0-9a-zA-Z_]

\D anything that’s not a number

\S anything that’s not a space

```

27. What is the use of the method "named_capture" in Regexp?

It will return a hash representing information about named captures of rxp.

A key of the hash is a name of the named captures. A value of the hash is an array which is list of indexes of corresponding named captures.

Answer :

```ruby
/(?< foo >.)(?< bar >.)/.named_captures
#=> {"foo"=>[1], "bar"=>[2]}
```


28.What is the use of "to_c" method in String?


Answer :

It will return the complex form of the input sting.


```ruby
'9'.to_c #=> (9+0i)
'2.5'.to_c #=> (2.5+0i)
```


29. How you will get this string?(without concatenation)

```ruby
a = " 3"
```


"Ruby 3"

Answer :

```ruby
a = "3"
a.prepend("Ruby ")
puts a
```


30. What is the use of abs2 method in Complex class?


Answer :

gives square of the result

```ruby
Complex(5).abs2 =>25
```


31. What is the alternative way of expressing ‘if not’.?

Answer :

```ruby
unless
# if !(aDay == 'Saturday' or aDay == 'Sunday')

unless aDay == 'Saturday' or aDay == 'Sunday'
daytype = 'weekday'
else
daytype = 'weekend'
end

return daytype

```

32. How "loop" keywords can be used in Ruby?

Answer :

```ruby
loop do

end


i=0
loop {
  puts(arr[i])
  i+=1
  if (i == arr.length) then
    break
  end
}

```

33. What is the difference between #remove_method and #undef_method?

Answer :

#undef_method( )
removes all methods, including the inherited ones.

#remove_method( )
removesall the methods, incase of inheritance, it leaves inherited methods.

```ruby
class A 
    def x
        puts "x from A class"
    end
end

class B < A
    def x
        puts "x from B Class"
    end
    undef_method :x
end


obj = B.new
obj.x



class A 
    def x
        puts "x from A class"
    end
end

class B < A
    def x
        puts "x from B Class"
    end
    remove_method :x
end

obj = B.new
obj.x
```
34. Is there an equivalent of “continue” in Ruby?

Answer :

The Ruby next statement is used to skip loop's next iteration. Once the next statement is executed, no further iteration will be performed.

The next statement in Ruby is equivalent to continue statement in other languages.

```ruby
for i in 5...11   
  if i == 7 then   
    next   
  end   
 puts i   
end  
```
35. How to display the inbetween values in a range?


print (1..7) #=> [1, 2, 3, 4, 5, 6, 7]

Answer :

entries, to_a

35. Refactor this code using reduce method
```ruby
def sum(array)
  sum = 0
  array.each do |number|
    sum += number
  end
 return sum
end

p sum([5, 10, 20])
# => 35
```
Answer : 

```ruby
def sum(array)
  array.reduce(:+)
end
p sum([5, 10, 20])
```


The ‘reduce’ method can be used to take an array and reduce it to a single value.


36. How can we print the minimum and maximum value from an array using a single method?

Answer :

#minmax

Return both minimum and maximum values from an array

```ruby
puts [2,4,55,0,45].minmax

#0,55
```
