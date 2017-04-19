# Ruby vs. JavaScript: Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ruby vs JavaScript](http://agentcooper.io/js-ruby-comparison/)

## Ruby vs. JavaScript: Compare and Contrast

Describe three examples of differences between Ruby and JavaScript.

```md

-Javascript is a front end language, Ruby is a back end language
(not a 100% clean distinction because of node.js)
-You don't need to use "var" in Ruby, you can just define a variable by assigning it
-Many functions/methods in Ruby have implicit returns, so you don't need to type "return" or console/log
-You use "do" in Ruby instead of curly brackets when you're telling the function what to do
-The syntax for functions is different in general. Don't have to type "function", for one

<!-- used:
(http://agentcooper.io/js-ruby-comparison/) -->
```

## Ruby vs. JavaScript: Type Conversion

Type conversion in Ruby is invoked by calling methods like `to_i` (to integer),
`to_f` (to float), and `to_s` (to string).  Here is some Ruby code that
declares two variables `left_operand` and `right_operand` to the strings `1` and
`2`, respectively.  It then declares a variable called `sum` that converts both
`left_operand` and `right_operand` to integers to add them.

```ruby
left_operand = '1'
right_operand = '2'

sum = left_operand.to_i + right_operand.to_i
# sum: 3
```

Write some JavaScript code that duplicates this functionality.

```javascript

const leftOperand = '1';
const rightOperand = '2';

const sum = (parseInt(leftOperand) + parseInt(rightOperand));

// used:
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/parseInt

```

## Ruby vs. JavaScript: String Interpolation

String interpolation in JavaScript is performed by wrapping a string with accent
graves (\`) rather than single quotation marks (') or double quotation marks
(").  For example,

```javascript
const beverage = 'tea'

console.log(`Many people drink ${beverage}.`)
// Output: Many people like to drink tea.
```

Write some Ruby code to duplicate this functionality.

```ruby

beverage = "tea"
puts "Many people drink #{beverage}"
end

# used:
# ruby-array training module
```

## Ruby vs. JavaScript: Array and String Methods

Use what you know about Ruby to do some string manipulation.  If you need to
look up Ruby's array and string methods, then check the
[Array](https://ruby-doc.org/core-2.3.1/Array.html) and
[String](https://ruby-doc.org/core-2.3.1/String.html) articles on
[Ruby-Doc.org](https://ruby-doc.org).

1.  Open `pry` in your terminal and set a variable, `str`, to `"eeffoc"`.
1.  Reverse the string so that the output reads `"coffee"`.
1.  Change the string into an array of characters so that the output reads
    `["c", "o", "f", "f", "e", "e"]`.
1.  Change your new array back into a string with hyphens in between characters
    so that your result is `"c-o-f-f-e-e"`.

```ruby

str = 'eeffoc'
str.reverse!
str = str.split('')
str = str.join('-')

# used:
# https://ruby-doc.org/core-2.2.0/String.html
```

## Ruby vs. JavaScript: Classes and Instantiation

Ruby has classes just like JavaScript, but while JavaScript uses prototypal
inheritance, Ruby uses class-based inheritance.  Here is some Ruby code that
declares a class called Person that takes an argument, `name`, upon
instantiation and sets it as an instance variable.  It also has a method named
`hello` that outputs a string to the console.

```ruby
class Person
  def initialize(name)
    @name = name
  end

  def hello
    puts "Hello, my name is #{@name}."
  end
end

boomhauer = Person.new('Jeff Boomhauer')

boomhauer.hello
# Output: Hello, my name is Jeff Boomhauer.
```

Write some JavaScript code that duplicates this functionality.

```javascript

const Person = function(name) {
  let helloName = name
}

Person.prototype.hello = function() {
  console.log(`Hello, my name is ${helloName}.`)
}

const boomhauer = new Person('Jeff Boomhauer')

boomhauer.hello()

// used:
// prototype documentation on MDN
```

## Ruby vs. JavaScript: Blocks and Callbacks, Part I

In Ruby, blocks are like anonymous functions that can be passed into methods,
but cannot be referenced again later on; similar to callback functions in
JavaScript.  Here is some Ruby code that takes an array of natural numbers and
filters out the ones that are not multiples of 3.

```ruby
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

filtered_numbers = numbers.select { |number| number % 3 == 0 }
# filtered_numbers: [3, 6, 9]
```

Write some JavaScript code that uses the array `filter()` method to duplicate
this functionality.

```javascript

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

const filteredNumbers = numbers.filter(number => number % 3 === 0)

// used:
// MDN filter documentation. 

```

## Ruby vs. JavaScript: Blocks and Callbacks, Part II

Here is some JavaScript code that takes an array of natural numbers and uses
`map()` to create a new array containing the squares of `numbers`.

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

const squares = numbers.map(number => {
  return number ** 2
})

// squares: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

Write some Ruby code that uses the Array `map` method and code blocks to
duplicate this functionality.

```ruby
# your answer here
```
