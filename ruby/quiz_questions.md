
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
a)Regexp.new( ‘string pattern' ,[ options ] )
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

▲

37. What does the following code print?

```ruby
def add(x, y)
  return(x + y)
end

result = add(4, 5) do
  puts "Hey Ruby"
end

p result
    
9
```
Answer :

The add() method is passed a code block, but it doesn't require the code block. When methods are passed a code block but don't require the code block, the code block is simply ignored.
  
38.is this valid code?

```ruby

class Learning
  def i_learn
    x = 'ruby'
    y = 'rails'
    z = 'sqlite3'
   
  end
end

b = Learning.new.i_learn
p eval('"The #{self.class}, the #{x}, the #{y}, the #{z}"', b)
```

How can we get this output?

```ruby

output 
"The Learning, the ruby, the rails, the sqlite3"
```
Answer : 

Binding objects can be used as the second argument of eval() to set the scope. The string of code passed as the first argument in eval() is evaluated in the context of the binding passed in the second argument.
  
39. Add code to the following class so 

```ruby

Motivation.new.speak returns "Go speed racer!!!"

first = 'speed'
second = 'racer'
class Motivation
  def speak
    # add code here
  end
end
```
Answer :

The TOPLEVEL_BINDING constant refers to the top level object. Note that this code will not work if it's pasted into the IRB console, this code must be run from a file with the normal Ruby interpreter.
  
40. What does the following code print? Explain.

```ruby

class A
  private
  def method_missing(name, *args)
    args.unshift(name.to_s).join
  end
end

p A.new.meta('programming', 'ruby')
    
"metaprogrammingruby"
```
Answer :

The name parameter is assigned to the method name (:meta) and args is assigned to an array of the arguments (['programming', 'ruby']).
  
41. What does the following code print? Explain.
```ruby

class Human
  def Human.about; end
  def self.generation; end
  def hi; end
  instance_eval do
    def bye; end
  end
end

p Human.singleton_methods
    
[:about, :generation, :bye]
```
Answer :

There are several ways to define singleton methods. Notice that the Human#hi method is a regular instance method and is not a singleton method.
  
42. What does the following code print? Explain.

```ruby

class Soccer
  @fun = 'woo hoo'
  def initialize
    @goal = 'score'
  end
end

s = Soccer.new
p s.instance_variables
    
[:@goal]
```
Answer :

The @goal instance variable is bound to instances of the Soccer class. The @fun instance variable is bound to the Soccer class object itself, not instances of the Soccer class.
  
43. Compare eql? and edual? methods
    
Answer :

eql? – Checks if the value and type of two operands are the same (as opposed to the == operator which compares values but ignores types). For example, 1 == 1.0 evaluates to true, whereas 1.eql?(1.0) evaluates to false.

equal? – Compares the identity of two objects; i.e., returns true if both operands have the same object id (i.e., if they both refer to the same object). Note that this will return false when comparing two identical copies of the same object.
  
44.How do you remove nil values in array using ruby?

Answer :

```ruby

>> [nil,123,nil,"test"]
=> [123, "test"]
    
>> [nil,123,nil,"test"].compact

=> [123, "test"]

```  
45. 
```ruby

if false
  value = 'test'
end
```
What will be the value of:

defined? value
defined? none

Answer :
```ruby

defined? value
#=> "local-variable"
defined? bar
#=> nil
```
46. Can you call a private method outside a Ruby class using its object?

Given the class Test:

```ruby

class Test
   private
       def method
         p "I am a private method"
      end
end
    
>> Test.new.send(:method)
"I am a private method"

```
Answer :

Yes, with the help of the send method.
  
47. What does the following code print? Explain.

```ruby

class Pencil; end

p Pencil.class
p Pencil.superclass
```    
>Class
>Object

Answer : 

All class objects (objects that can be used to instantiate other objects) are instances of the Class class. Hash.class, Array.class, String.class, and Pencil.class all return Class.
  
48. What does the following code print? Explain.

```ruby

p BasicObject.superclass

```  
Answer : 

nil
Every class object (i.e. instance of the Class class) has a superclass, except for BasicObject. BasicObject is at the top of the class hierarchy and does not have a superclass.
  
49. What does the following code print? Explain.

```ruby

p BasicObject.singleton_class.superclass
```

Answer :

Class
BasicObject's singleton class inherits from Class.
  
50. 
```ruby

versions = {:ruby=>"3"}
```
What is the difference between the following lines of code?

```ruby

versions[:rails]
versions.fetch(:rails)
```
Answer : 

versions.fetch(:rails) raises an exception because the :railskey is not present in the versionshash (if a second argument was added to the fetch() method, the default value would be returned instead of raising an exception).

versions[:rails] returns nil because the :rails key is not present in the versions hash.
  
51. What is the output of this code?
```ruby

def dubSplat(a, *b, **c)  
        p b
  p c
end
    
dubSplat(1,2,3, 4, a: 40, b: 50)
``` 
Answer : 

=> [2, 3, 4]
You can also use the splat operator(*) to grab any segment of an array
The double splat operator (**) can be used for hashes!
=> {:a=>40, :b=>50}
52. What is Spaceship Operator in Ruby? How it is working?

```ruby
a <=> b 
```

Answer : 

  if a < b then return -1
  if a = b then return  0
  if a > b then return  1
  if a and b are not comparable then return nil
  
53. What is the name of this operator? How it will work?

===

Answer : 
   
subsumption operator.

 "If a described a set, would b be a member of that set?"

```ruby
(1..5) === 3           # => true
(1..5) === 6           # => false

Integer === 42          # => true
Integer === 'fourtytwo' # => false
```
54. True or False?

```ruby
>count ||= 0
```
Answer : 

count ||= 0 gives count the value 0 if count is nil or false.
    
True

a ||= b
The assignment statement supports a set of shortcuts: a op= b is the same
as a = a op b. This works for most operators:
count += 1 # same as count = count + 1
price *= discount # price = price * discount
count ||= 0 # count = count || 0
So, count ||= 0 gives count the value 0 if count is nil or false.

55.

```ruby
string = "Ruby" + " 3" 
  
string = "Ruby" "3" 
  
string = "Ruby" << " 3." 
  
string = "Ruby".concat("3")

```
puts string  

Answer : 

"Ruby 3"

Which one is false?
    
All are true

there are 4 ways to do string concatenation
  
56. What does the following code return?

```ruby
book = ["intelligent investor"]
great_book = ["intelligent investor"]

book.object_id == great_book.object_id
```
Answer : 

false

The book and great_book arrays have the same content, but are different instances of the Array class and therefore have different object_ids. Array equality comparisons in Ruby check if arrays have the same content in the same order, not if the arrays are the same exact object.
  

57.What would be the output?
```ruby
class Monster
  private
  def method_missing(name, *args)
    puts "blah monster, attack!"
  end
end

ob = Monster.new

ob.method :output
ob.method :name

ob.name
ob.output

```   
Answer : 

ob.name alone will give output. rest of the ob.method will raise errors.
  
58. What would be the output?

```ruby
class Mammal
  def self.about
    "we are living creatures"
  end
end

class Dog < Mammal; end

p Dog.about

```
Answer : 

"we are living creatures"


Class methods are also inherited.
  
59. What are differences in these two class definitions?

```ruby
#Class Definition #1
class Cat < Object
end

#Class Definition #2
class Cat
end

```
Answer : 

There is no difference between Class Definition #1 and Class Definition #2. Class Definition #1 explicitly inherits from Object, but Class Definition #2 inherits from Object by default (implicitly), so these class definitions are identical.
  
60. What does the following code print? Explain.

```ruby
module X; end
module Y; end
class Z
  include Y
  include X
end

p Z.ancestors
```
Answer : 
 
[Z, X, Y, Object, Kernel, BasicObject]
When Y is included, it is added immediately to the right of Z in the ancestors chain. When X is included, it is added immediately to the right of Z in the ancestors chain, thus moving Y one position to the right.
  
61. Is this Valid code?

```ruby
module Batman
  def self.sidekick
    'robin'
  end
end

p Batman::sidekick
    
'robin'

```
Answer : 

Singleton methods of a module can either be called with dot notation (Batman.sidekick) or :: notation (Batman::sidekick).
  
62. Is this valid?

```ruby
class Dog; end
dog = Dog.new
def dog.bark
  "ruff ruff"
end


p dog.bark
```   
"ruff ruff"
Answer : 

dog is an instance of the Dog class and is given a singleton method bark(). The bark() method can be called on the dog instance of the Dog class, but is not available for other instances of the Dog class.

  
63. What is the difference between Explicitly casting and  implicitly coercing types in Ruby?
  
Answer : 

The most common casting helpers are #to_s, #to_i, #to_a and #to_h. These are explicit casting methods. They help us easily transform a value from one type to another.


Ruby also offers implicit coercion methods which only return a value when objects act like the type. This way we can be sure that the value acts like the type we want. These implicit coercion methods are #to_str, #to_int, #to_ary and #to_hash
  
64. What is the use of Undef Keyword?
    
Answer : 

Ruby provides a special keyword which is known as undef keyword. This keyword used to avoid the current working class from responding to calls to the specified named methods or variable.
  
65. Which one is not a reserved keyword in Ruby?

a)defined?
b)alias
c)_ _FILE_ _
d)nil

Answer : 
  
All are reserved keywords
  
66. If we do dynamic modification to a class (means to add new or overwrite existing methods) at runtime that technique will be called as ?

Answer : 

In Ruby, a Monkey Patch (MP) is referred to as a dynamic modification to a class and by a dynamic modification to a class means to add new or overwrite existing methods at runtime.
  
67. What would be the output of this code?


```ruby
h1 = {a: 1, b: 2}
h2 = h1.merge!({lala: "word up"})
puts h1.object_id == h2.object_id
```

Answer : 

true

The Hash#merge! method combines two hashes and mutates the original hash. Since the haha and bozo variables are assigned to the same object, they have the same object id. If the Hash#merge method was used (notice no !), then the original object would not have been mutated and the object ids would be different
  
68. what is the user of this operator?

!~

```ruby   
if "Ruby Quicktips" !~ /\d+/
  puts "The string does not contain any digits."
end
# The string does not contains any digits.
# => nil
``` 
69.How to print this output?

30 29 28 27 26 25

Answer : 

```ruby   
30.downto(25){ |i| puts i}
```
The downto() function in Ruby returns all the numbers less than equal to number and greater than equal to limit.
  
70.What is the use of partition method in string?


Answer : 

```ruby   
partition(sep) → [head, sep, tail]

"hello".partition("l")         #=> ["he", "l", "lo"]
"hello".partition("x")         #=> ["hello", "", ""]
```

71. What does the following code print? Explain.

```ruby
h = {}
class Sublime
@fav = 'caress me down'
def sing(obj)
obj.instance_variable_set(:@greeting, 'mucho gusto')
obj.instance_variable_set(:@name, 'me llamo brad lee')
end
end

s = Sublime.new
s.sing(h)
p s.instance_variables
p "***"
p h.instance_variables
```

Answer : 

[]
"***"
[:@greeting, :@name]


In this example, the instance variables are bound to a specific object and are not bound to self by default.

72.What does the following code print? Explain.

```ruby
class Object
private
def method_missing(name, *args)
'This is a terrible idea'
end
end

p 'string'
p 'boo'.fooey
p 'array'
p [].boggie_down

Answer : 

```
'string'
'This is a terrible idea'
'array'
'This is a terrible idea'

Object#method_missing is called before the default BasicObject#method_missing can be called. This code would return 'This is a terrible idea' for almost all messages sent to objects that inherit from Object cannot respond to. It's terrible code, but illustrates the method_missing lookup process and how instances of different classes can share the same method_missing.


73. What does the following code print? Explain.

```ruby
class RubyGuide
  class << self
    p self
    p self == RubyGuide.singleton_class
  end
end
```

Answer : 

#
true

74. What is the output of this code?
```ruby
require 'date'
(4.days + 5.weeks).from_now
```

Answer : 

Error
You need active support in rails to do that


75. How to print this output?

30 29 28 27 26 25

Answer : 

30.downto(25){ |i| puts i}

The downto() function in Ruby returns all the numbers less than equal to number and greater than equal to limit.

76. Which of the following methods can be used in Ruby to get a random number?

a) rnd

b) Math.GetRandomNumber

c) $random

d) rand

Answer : 

rand(1..10)

77. Difference between "require" and "load" in module?


Answer : 

Require reads the file from the file system, parses it, saves to the memory, and runs it in a given place. In require, if you modify the specified file when the script is running, those modifications won’t be applied, Ruby will use the file from memory, not from the file system of the machine.

Load reads and parses files every time the file (in which load is called) is executed

78. How can you run some ruby script without IRB or ruby file?

We can use the -e tag against the ruby command.

Answer :
```ruby
>ruby -e 'puts "Ruby programming"'
```

79. What would be the output of the code?

```ruby
puts "This statement comes later"
BEGIN {
puts "This statement will be printed in the beginning"
}
```

Answer :
```ruby
This statement will be printed in the beginning
This statement comes later
```

80. It is possible to print multi-line strings using print in Ruby?

Answer :

yes

We can use "Here Document"

```ruby
print <<`EOC`                 # execute commands
echo First Statement
echo Second Statement
EOC
```

```ruby
print <<EOF
Multiple line string.
First wayEOF
              # same as above
Multiple line string.
Second way
EOF
```

You can also use,

```ruby
print "\n I am also multiline string 
  \n you can use this too
end"

```

81. What would be the output?

```ruby
"[%s]" % "same old drag"
```

Answer :

=> "[same old drag]"

This is quick string interpolation


82. 
```ruby
x = %w{p hello p}
puts "<%s>%s</%s>" % x 
```

is this valid?

Answer :

yes. It is also Interpolation

```ruby
<p>hello</p>
```

83. What is the output of this code?

```ruby
a = %w{a b}
b = %w{c d}

[a + b]
[*a + b]
```
Answer :

[a + b] # => [["a", "b", "c", "d"]]
[*a + b] # => ["a", "b", "c", "d"]

84. 
```ruby
does = is = { true => 'Yes', false => 'No' }

does[10 == 50]
is[10 > 5]
```

is this valid ?


Answer :

It's rare you see anyone use non-strings or symbols as hash keys. It's totally possible though, and sometimes handy.

```ruby
does[10 == 50] # => "No"
is[10 > 5] # => "Yes"
```
85. 
```ruby
require 'rubygems'
require 'activemerchant'
require 'date'
```
If we have more required modules, shall we use any shortcut code for this?

Answer :

you can take this to extremes using Ruby's enumerators to perform similar operations multiple times. Consider requiring multiple files, for instance:

```ruby
%w{date json rubygems}.each { |x| require x }
puts Date.today
puts JSON.parse('{"desc":{"someKey":"someValue","anotherKey":"value"},"main_item":{"stats":{"a":8,"b":12,"c":10}}}')
```

86. 
```ruby
qty = 1
qty == 0 ? 'none' : qty == 1 ? 'one' : 'many'
```
is this valid code?

What would be the output?

Answer :

"one"

ternary operators can be nested within each other

87. How to skip this error?

```ruby
h = { :age => 10 }
h[:name].downcase =>Error
```


Answer :
yes.
You can use rescue in its single line form to return a value when other things on the line go awry:

```ruby
h = { :age => 10 }
h[:name].downcase # ERROR
h[:name].downcase rescue "No name" # => "No name"
```

another way
```ruby
h.fetch(:name,"no name")
```

88. How to delete directories with files in Ruby?

To delete directories, Ruby comes with a handy file utility library called FileUtils that can do the hard work:

Answer: 

```ruby
require 'fileutils'
FileUtils.rm_r 'somedir'
```
89. 
```ruby
money = 9.5
cost = 100

```

How to convert the above to "9.50" and "100.00"?

Answer :

Formatting floating point numbers into a form used for prices can be done with sprintf or, alternatively, with a formatting interpolation:
```ruby
money = 9.5
cost = 100
puts "%.2f" % money 
puts "%.2f" % cost 
```

90. 
```ruby
a = %w{a b c d e f g h}
b = [0, 5, 6]

a.values_at(b[0])
a.values_at(b[1])
a.values_at(b[2]) # a , f, g
```
How to get the values in one shot?

Answer :

```ruby
a = %w{a b c d e f g h}
b = [0, 5, 6]
a.values_at(*b).inspect
```
use explode