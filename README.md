# The Assignment Expression

## Learning Goals

* Define the _Assignment Expression_
* Define Mutability / Immutability
* Constant versus "Symbolic Constants" and "Values"
* Return Value of an _Assignment Expression_

## Introduction

So you've seen the first of our **essential three expressions**, the _constant
expression_ which gives Ruby some constant fact about the world: `2` is `2`.

It's really useful to associate an _expression's_ _evaluated_ result with a
'name'. We call those names that we associate with the _expression's_ result,
_variable names_ or, commonly, just _variables_. The process of bonding an
expression to a variable is called _assigning a variable_. Programmers also say
that "the variable name 'points to' the expression that was assigned to it."

Some helpful metaphors here are it's like adding a new entry to a dictionary
`a_fun_number`'s definition is `3 * (10 -6)` or `my_birth_year` is `1929`.

![Variable naming as dictionary entry](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-assignment-expression/Image_87A_VariableNamingMetaphors.png)

Or a variable name is like a label you put on a box:

![Variable naming as labeled box](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-assignment-expression/Image_87C_VariableNamingMetaphors.png)

We use the second of our **essential three expressions** to do this: the
_assignment expression_.

## Define the _Assignment Expression_

In Ruby, the assignment expression is like so:

![Assignment Expression Graphic](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-assignment-expression/Image_88_AssignmentExpression.png)

Here are some examples:

```ruby
a_fun_number = 3 * (10 - 4)
my_birth_year = 1929
```

Variables names are most often lower case descriptions of what their assigned
expressions _mean_. When the words need to be separated we use `_` to act like
a "space". While you _can include_ some numbers and symbols as variable names,
let's keep things simple for the moment and just use lower-case letters and
`_`.

When we define a variable using the "assignment expression" we add
something new to Ruby itself.

Consider this IRB conversation:

```ruby
irb(main):001:0> maximum_speed
NameError (undefined local variable or method `maximum_speed' for main:Object)
irb(main):002:0> maximum_speed = 55
=> 55
```

Here, Ruby, by default, doesn't know anything about `maximum_speed`. After
"defining the variable `maximum_speed`, it did.

> ***SUPER-IMPORTANT***: In the assignment expression `=` means "assignment" it
> does not mean "what's on the left of the `=` is equal to what's on the left."
> In math courses, we use `=` to say that the expressions on either side of the
> `=` are the same. Ruby uses `==` for _that_ purpose. It's very confusing for
> beginners to have bugs where they confuse `=` for `==`.

## Define Mutability / Immutability

A variable is said to be "mutable." That means the value that the name "points
to" can be changed during the running of the program. Being able to change the
value a variable points to is very important. If we need to do something 10
times or until the page loads, we need to be able to count how many times
something happens. Here's "mutability" in action:

Many years ago I was:

```ruby
height_in_centimeters = 50
```

But today I am:

```ruby
height_in_centimeters = 180
```

We can try these out in IRB:

![Variable Asignment](https://curriculum-content.s3.amazonaws.com/prework/mutable_var_assn.gif)

Sometimes, we might want to make a variable name permanent. We might want to
say "hey, this value should not change." We want to say that the value is
_immutable_, the opposite of _mutable_. We do this by writing a "constant." In
Ruby, constants are assigned just like variables, **except** their names are
written in `ALL_CAPS`.

```ruby
SPEED_OF_LIGHT = 180000
```

If, after this, you try to set `SPEED_OF_LIGHT` to something else, Ruby will
complain.

```ruby
SPEED_OF_LIGHT = 1800000
warning: already initialized constant SPEED_OF_LIGHT
```

![Constant Assignment](https://curriculum-content.s3.amazonaws.com/prework/constant_assn.gif)

Programmers call an assignment to a variable that is meant to be
"not-change-able" or immutable, "setting a constant."

Sometimes we want the programming language to yell at us if we try to change
the value of certain variables. In real life, changing the value of the speed
of light would be very bad for existence in this universe. If we had a program
for doing space travel written in Ruby, we might want it to yell at us if we
tried to change this constant's value.

## Return Value of an _Assignment Expression_

It's interesting, but the return value of an _assignment expression_ is the
evaluated result of the expression to the right of the `=`.

```ruby
recurring_expression_value = 3 * (10 - 6)
=> 18
```

Pay attention here, the return value of the assignment expression ***IS NOT THE
SAME THING*** as getting the value out of the variable name. We'll learn to get
the variable "back out of a variable" in the next lesson. What Ruby's saying is
that the assignment expression's return value is the value of the expression to
the right of the `=`.

## Conclusion

Think about a baby who has never spoken before.  Before it, stands a parent
saying their name over and over (...and over) again.

![Learning to talk 1](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-assignment-expression/Image_55_Mama-Baby_1.png)

They wave towards their bodies and say their names again and again. What the
parent is trying to do is teach the baby to assign their face to the variable
name "Mama" or "Dada." But to the baby, this means nothing.

While neither the baby or the (average) adult is aware of it, they're trying to
teach the baby the second of the _three essential expressions_: the assignment
expression. Then, one magical day, it clicks for the baby. It performs an
assignment in its precious little head:

![Learning to talk 2](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-assignment-expression/Image_55_Mama-Baby_2.png)

Unfortunately, Mom is still sad, she doesn't have any _proof_ that the
assignment was successful. For that to work, the baby will need to prove that
it can "look up" the variable assignment of who "ma-ma" points to. We'll need
to teach Ruby, and baby will need to learn the last of our _essential
expressions_: the variable lookup expression!
