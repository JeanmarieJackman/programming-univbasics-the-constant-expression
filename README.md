# The Constant Expression

## Learning Goals

* Identify the _constant expression_
* Explain how the _constant expression_ stops evaluation

## Introduction

Lets repeat our definition of _expression_

> **Definition**: Expression: A combination of information called _data_ and
> _symbols_ indicating how to combine _data_ called _operators_.

What if we were to make an expression that had no _operators_? What if it only
had _data_. Here we're giving just such a thing to Ruby in IRB.

![IRB Constant Expression](https://curriculum-content.s3.amazonaws.com/prework/constant_expr_animation.gif)

This expression is the _constant expression_ and it's very important, although
very boring.

It's boring because it doesn't _do_ anything except be itself. But it's
important because it confirms that Ruby knows when to stop applying operations.
It tells Ruby to _stop_, you have an answer.

### Explain How the _Constant Expression_ Stops Evaluation

Let's consider a simple arithmetic expression. Keep in mind we apply operators
in "[PEMDAS][]" order: parenthesis, exponents, multiplication, division,
addition, subtraction.

We'll start with the expression:

![Math Expression: Step 0](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-constant-expression/Image_54_Step0.png)

Ruby's mission is to find a constant piece of data or a _constant expression_.
Because of `()`, it goes there first. The `(10 - 4)` is clearly **not** a
constant expression because of the `-` operator's presence. Ruby makes a "tree"
of the two sides of the operator (`-`) and then looks on each side to see
whether those sides are _constant expressions_ i.e. "plain old data."

![Math Expression: Step 1](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-constant-expression/Image_54_Step1.5.png) 

Eventually it reaches `4` and that's plain old data. It then checks the other
side and sees `10`, _also_ plain old data.

![Math Expression: Step 1.5](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-constant-expression/Image_54_Step2.png)

Since these two are constant expressions, it can apply `-` to them and produce
`6` &mdash; a _constant expression_.

So what Ruby now sees looks like this:

![Math Expression: Step 2](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-constant-expression/Image_54_Step4.png)

By the same logic of what we saw inside the `()`, Ruby then applies the `*` to
`3` and `6` and creates a new expression, a _constant expression_ the answer
(or "return value"):

![Math Expression: Step 3](https://curriculum-content.s3.amazonaws.com/programming-univbasics/the-constant-expression/Image_54_Step5.png)

Whew! Fortunately, Ruby does _all this work_ of building a tree of operators
and returning a value very quickly!

The _constant expression_ is _always_ the last expression in a complex
expression. It's how Ruby knows it has _data_ that it can work with and that no
other operations need to be applied.

## Table Explanation

Another way of looking at this process might be to look at a table. We'll
repeat all the same things we just showed graphically, but if a table makes
more sense for you, then you'll like this one better!

This is an important tool when learning to program, if you like thinking in
code, try out the code; if you prefer diagrams, draw the diagram. An important
part of learning to be a technologist is learning to build the technology you
need to learn more technology.

| Expression       | Has Operators? | Operators | Are we done? | Which to Apply |
| ---------------- | -------------- | --------- | ------------ | -------------- |
| `3*(10-4)` | YES            | `*`, `()` | NO           | Zoom-in on new sub-expression in `()` because of [PEMDAS][]|
| `(10-4)`     | YES            | `-`       | NO           | Evaluate sub-expressions|
| `10`             | NO             | NONE      | YES          | Zoom in on expression `10`. Constant expression! Return the value of the constant, we're done!|
| `4`              | NO             | NONE      | YES          | Zoom in on expression `4`. Constant expression! Return the value of the constant, we're done!|
| `(10-4)`     | YES            | `-`       | NO           | Replace `( 10 - 4 )` with application of `-` to `10` and `4` making `6`
| `3*6`          | YES            | `*`       | NO           | Zoom-out and replace the sub-expression with its value we just determined|
| `3*6`          | YES            | `-`       | NO           | Zoom-in on sub-expression|
| ` 3`             | NO             | NONE      | YES          | Zoom in on expression `3`. Constant expression! Return the value of the constant, we're done!|
| `6`              | NO             | NONE      | YES          | Zoom in on expression `6`. Constant expression! Return the value of the constant, we're done!|
| `3*6`          | YES            | `*`       | NO           | Replace `3 * 6` with application of `*` to `3` and `6` making `18`|
| `18`             | NO             | NONE      | YES          | Constant expression! Return the value of the constant, we're done!|

## Conclusion

While the _constant expression_ might seem dull, it lets us know when
expression evaluation is done _and_ establishes a groundwork for all the
following expressions. The first rule of Aristotle's logic is `A is A`; the
constant expression provides a similar "foundation" for programming.

[PEMDAS]: https://en.wikipedia.org/wiki/Order_of_operations

