# variable types

Keyword `my` is used to create a local variable.
Without it, the variable will be treated as globle.

## scalar

Scalar variable is preceded with `$` while creating it.

Expressions that yield scalar variable begin with `$`.

**The way an expression is evaluated depends on context**:
- In an assignment statement, the left side determines the context.
  If the left side is a scalar, the right side is evaluated in scalar
  context. If the left side is an array, the right side is evaluated
  in list context.

## array

Arrays are preceded with `@` mark.

Expressions that yield arrays  begin with `@`.

Initializing an array with literal lists:

```
# (1,2,3) is a literal list
my @list = (1,2,3)
```

> Note: there is some minor difference in literal
> lists and arrays. When we assign a literal list
> to a scalar, the scalar variable get the last variale
> in the list. If we assign an array to an scalar
> variable, the scalar get the length. See the following
> example.

```
my $scalar1 = (1, 2, 4)
# the value of $scalar1 is 4

my @array1 = (1, 2, 4)
my $scalar2 = @array1

# the value of $scalar2 is 3
```

Accessing elements of an array.

```
print @array[0]
```

Getting the length of an array:



Slicing an array.

```
my @words = @array[0, 2]
```