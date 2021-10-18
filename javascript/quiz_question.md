[Question1:What is the name of called? ](#question1)  



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






## Question1


this is test
this is test
this is test
this is test
script




