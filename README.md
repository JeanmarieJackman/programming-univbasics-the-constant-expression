# The Constant Expression

## Learning Goals

* Identify the _constant expression_
* Explain how the _constant expression_ stops evaluation
* Explain how the _constant expression_ creates agreement

## Introduction

Our definition of _expression_ is:

> An expression in a programming language is a combination of one or more
> constants, variables, operators, ... that the programming language
> interprets (according to its particular rules of precedence and of association)
> and computes to produce ("to return", in a stateful environment) another value.
> This process, as for mathematical expressions, is called evaluation.

[Wikipedia][def]

What if we were to make an expression that had no _variables_, since we haven't
learned about them yet (but will soon!). What if it _also_ didn't have
_operators_? That would be an expression like:

```ruby
42
```

This expression is the _constant expression_ and it's very important, although
very boring from a programming as conversation perspective, the _constant
expression_ has the power to create _agreement_ and _trust_. And if it weren't
for your ability to agree with our conversational partner about basic reality,
programming would never have been possible!

## Define the _Constant Expression_

The constant expression is an expression composed only of _constants_. Its
_return value_ is the same as the constants.

## Importance of the _Constant Expression_

### Explain How the _Constant Expression_ Stops Evaluation

This _expression_ is important because it tells Ruby _when to stop_.

Let's consider a simple arithmetic expression. Keep in mind we apply operators
in "[PEMDAS][]" order: parenthesis, exponents, multiplication, division,
addition, subtraction.

| Expression       | Has Operators? | Operators | Are we done? | Which to Apply |
| ---------------- | -------------- | --------- | ------------ | -------------- |
| `3 * ( 10 - 5 )` | YES            | `*`, `()` | NO           | Zoom-in on new sub-expression in `()` because of PEMDAS|
| `( 10 - 5 )`     | YES            | `-`       | NO           | `-` because of PEMDAS|
| `5`              | NO             | NONE      | YES          | Constant expression! Return the value of the constant, we're done!|
| `3 * 5`          | YES            | `*`       | NO           | Restate with the return value of the inner expression|
| `3 * 5`          | YES            | `*`       | NO           | `*` because of PEMDAS|
| `15`             | NO             | NONE      | YES          | Constant expression! Return the value of the constant, we're done!|

> **DEBUGGING TIP** This table might remind you of a "proof" from geometry. It
> shows how to "step into" an expression (or a sub-expression); and
> methodically trace the return values back out. This is a great tool for
> debugging!

> **PONDER** Note that "Are we done?" is the truth reverse of "Has Operators?"
> If only somehow there were a way to reverse a truth value in programming,
> maybe an operator that could reverse a constant value that's `true` or
> `false`. Keep reading!

The _constant expression_ is always the last expression in a complex
expression. But there's another reason why

### Explain How the _Constant Expression_ Creates Agreement

Open up IRB and give a _constant expression_ to Ruby.

![IRB Constant Expression](https://curriculum-content.s3.amazonaws.com/prework/constant_expr_animation.gif)

It just returns the value _we_ as intelligent humans we are, shrug and think of
this as "no big deal."

But lets imagine an alien species lands and, in an attempt to communicate, we
do a series of "mirroring" exercises. The movie "Arrival" covers some of this
ground:

![Can we match?](https://media.giphy.com/media/3o7TKuQo5VpLLVz6W4/giphy.gif)

"Mirroring" establishes "I see what you see" and "I can 'follow' your
analogies, we can build on this."

Earth. Shaking. Power.

From simple "mirroring" you can build to trading "what we call something"
versus "what you call something."

![Building on matching](https://media.giphy.com/media/3oriOeYGl5MKFtb2FO/giphy.gif)

Because of _agreement_ exists, we can _trust_ our conversational partner.  What
if when we told Ruby `1 + 1`, it returned `3`? Or what if _sometimes_ it
returned `99` and _other_ times `2.12`? How could we have agreement and trust
then? We'd lose our minds if the world appeared so disordered!

Shakespeare even played with the necessity of _agreement_

    Petruchio: I say it is the moon.
    Katherina: I know it is the moon.
    Petruchio: Nay, then you lie; it is the blessed sun.

&mdash; Shakespeare "Taming of the Shrew" Act IV, Scene V

We _need_ agreement. Ruby's evaluation of the simple constant expression agrees
with ours, and we will build all programming we ever learn from this
foundation.

## Conclusion

While the _constant expression_ might seem dull, it is the foundation of
communication with other intelligences, including Ruby. It lets us know when
expression evaluation is done, lets us be sure that we and the machine "agree,"
_and_ establishes a groundwork for all the following expressions.

[def]: https://en.wikipedia.org/wiki/Expression_(computer_science)
[PEMDAS]: https://en.wikipedia.org/wiki/Order_of_operations


