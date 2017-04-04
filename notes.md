When I was first introduced to Ruby, I asked, “Why Ruby?”  I got two common replies:

- It makes you think about programming differently (especially if you come from a non-OOP background).
- It makes you happy.

Ruby was designed from a programmer’s point-of-view for productivity. Its syntax is elegant and it’s a scripting language, like python, meaning you dont need to compile things.

```
> 1 + 23423434
=> 23423435
```

Quien me puede decir cual es ese numero de la derecha?
dos millones cuatrocientos veintitres mil cuatrocientos trenta y cuatro
medio dificil de leer huh?
in ruby we can also do this for legibility

```
> 1 + 23_423_434
=> 23423435
```

We also have strings 

```
> "My name is Victor"
=> "My name is Victor"
```

Ever wondered what does your name look backwards? 

```
> "Victor".reverse
=> "rotciV"
```

notice that we are not using parenthesis in order to execute a method.
Porque Ruby es Orientado a objetos, you used a dot to access a hidden list of methods that belong to all strings.
que pasa si lo hacemos con numeros?

```
> [1,2,3]
> [1, 'string', :symbol, Class]
```

arrays are also objects, objects which we can also call methods on
because of its dinamism you can have all types of objects inside an array.

```
> [1,2,3].max
=> 3
```

Estamos es un poco canson tener que escribir esa lista en una variable

```
multiline = "
this string
is divided 
in lines
"
> multiline.lines
> multiline.lines.reverse
```

ahi podemos comenzar a ver un poco de la legibilidad que te aporta ruby

```
> multiline.lines.each.with_index { |line, i | puts "Line #{i}: #{line}" }
```

So here we are grasping two concepts, a block and interpolation
a block is a chunk of Ruby code surrounded by curly braces.
interpolation is evaluating ruby code, where de "i" and "line" are, and putting that in the string.

```
> multiline.include?   "divided"
> multiline.gsub! 'this', 'this is not'
> puts multiline
```

Guess what? Methods can also have question marks.

Conventionally, methods with a ? at the end return boolean values. And methods with a ! perform some “dangerous” operation like mutating the String.

and lastly we have hashes, 
Hashes are associative Arrays (like dictionaries in other languages) and hold key-value pairs. The keys and values can be an object of any type.
```
> { key: "value", "a string as a key" => 1, symbol: :symbol }
```

Also notice that for every statement, the Ruby interpreter returns something, even if that something is nil. In Ruby, every statement is an expression and will result in a value.

```
def this_is_a_method
  puts "it prints me"
end
=> :this_is_a_method
```

For this reason, You can omit the return keyword in Ruby. The last line executed in a block of code is the value that is returned.

```
> puts "I'm true today" if condition
> puts "I'm false today" unless condition
```

another neat thing is how you can structure if statements for legibility.
You can use the unless keyword in place of if when you do not want to perform an action if the condition is true.
normal multiline if behave exactly as expected.

```
Class.is_a? Object
Class.methods
```

Hold on, you can use methods on classes?! Remember I told you that everything was an object? Well, your class definition happens to be an object of type Class with the constant Greet pointing to it. Don’t believe me? Try it out for yourself
Everything is an object, including integers and floating point numbers. We’ll come back to this in a bit. For people familiar with object oriented programming, it’s nice to see that everything is object oriented, even basic operations like the addition of numbers.

And how do we define classes?

```
Class Duck
  def quack
    "QUACK!"
  end
end

donald = Duck.new
donald.quack
```

If an object walks like a duck and talks like a duck, then the Ruby interpreter is happy to treat it as if it were a duck.

In Ruby, we rely less on the type (or class) of an object and more on its capabilities. Hence, Duck Typing means an object type is defined by what it can do, not by what it is. Duck Typing refers to the tendency of Ruby to be less concerned with the class of an object and more concerned with what methods can be called on it and what operations can be performed on it. In Ruby, we would use respond_to? or might simply pass an object to a method and know that an exception will be raised if it is used inappropriately.

and we can also modify the behavior of an already defined object and/or class
```
class << donald
  def quack
    'Hiya, toots!'
  end
end

donald.quack
```

Esto es llamado monkey patching es un feature que le da bastante flexibilidad al lenguaje.

```
define_method :square do |x|
x*x
end
```

Este otro feature se le llama metaprogramming y se refiere a la posibilidad de definir methodos, classes y objetos de manera dinamica.


Now show them how easy it is to make an webpage with sinatra

Sinatra is a DSL for quickly creating web applications in Ruby with minimal effort:

Then what is rails, Rails is a web-application framework that includes everything needed to create database-backed web applications according to the Model-View-Controller (MVC) pattern.

The process of programming is much faster than with other frameworks and languages, partly because of the object-oriented nature of Ruby and the vast collection of open source code available within the Rails community.
The Rails conventions also make it easy for developers to move between different Rails projects, as each project will tend to follow the same structure and coding practices.
