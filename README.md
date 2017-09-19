# Leap Year Challenge

## The Goal

We're going to write a program which will tell us whether or not a given year is a leap year. We'll do three versions of it - each one a little more complicated than the last.

To do this, you may want to use a <a href="https://www.accuracyproject.org/leapyears.html">list of which years are leap years</a>.

## The Lab

We'll separate our concerns by _defining_ our methods in the leap.rb file, and _calling_ our methods in the testleap.rb file.

Open up those two files, complete the challenges listed, and run your tests with the command `ruby testleap.rb`

## Skills you may need

### Comparison operators

You've already used some comparison operators (greater than, less than, and equals) in our last lab. You may want <a href="https://www.tutorialspoint.com/ruby/ruby_operators.htm">a few more</a>.

### Modulus and remainders

<details>
  <summary>Click here for a review of Ruby integer division</summary><br>

  In Ruby, Integer division can be tricky. If you have't tried dividing something that should result in a decimal (like 10/3), try it now.

  Since both inputs are integers, the return value of that division expression will _also_ be an integer. In other words, it's truncating the data (cutting off the decimal; rounding _down_ to the nearest integer). 10/3 in math class would be 3.333... repeating. But in programming, the decimal is chopped off (truncated), so 10/3 in Ruby is 3, because the expression of integers will be rounded down to the nearest integer.

  10/3 can also be written as 3r1 (three, with a remainder of 1) - and _that's_ the key to understanding the modulus.
</details><br>

In Ruby, you can easily find the remainder of a division expression of integers. For example, 10 divided by three is three, with a remainder of 1.

To jump straight to a remainder, can write the expression using the modulus (%) operator.

` 10 % 3 `

This expression will return the remainder - it will evaluate to 1.

##### Modulus uses

The modulus is used more often in computer programming than you might use remainders in your everyday life. One of the most common uses of a modulus is to check if a number is even or odd. Since `10 % 2` evaluates to 0 (there's no remainder), you know it's even. Since `9 % 2` evaluates to 1 (since nine divided by 2 is 4 with a remainder of 1), a lot of programs will check whether an integer is even or odd using code that looks like this.

```ruby
if some_number % 2 == 0
  puts "This number is even!"
elsif some_number % 2 == 1
  puts "This number is odd!"
end
```

### Boolean return data

The first method we will define will tell us whether a given year is a leap year. This is a really useful method, because there are only two possible answers. That's why we'll define this method with a question mark. In Ruby, a question mark is a way programmers communicate that the return value will be a true or a false - a boolean value, as they're called in programming.

```ruby
def is_leap_year?(year)
  if # some code to check and see if the year is a leap year.
    return true
  else
    return false
  end
end
```

Notice that the words true and false are not in quotes. If we wrote them that way, they'd be strings. We want boolean values, not strings, so we're not using quotes.

### for-in loops

Loops, as you might imagine, let you repeat something on a scale that would be exhausting to do manually. We will cover many types in our courses together, but here's a great first loop to run.

Let's write code that prints every number from 1-100:

```ruby
for x in 1..100
  puts x
end
```

In this loop, the letter x represents each number, one at a time. Generally it's called a local variable, and more specifically it will sometimes be referred to as an iterator.

The plain-words translation of that loop might read like this: `for every number in 1-100, print that number.`

This can become even cooler when we manipulate the code block inside the loop:

```ruby
for x in 1..100
  puts x * 2
end
```

The plain-words translation of that loop might read like this: `for every number in 1-100, print double the value of that number.`
