# Monotony

Generate and store monotonically increasing integers.

Sometimes you need a number that increases, like for instance a build number.
However, if you're outside of a build system, you might not have easy access a number like that.

Monotony will allow you to create and recall an arbitrary amount of numbers, storing the current number as it goes.

Monotony requires **Python3**.

## Usage

Create a new number and retrieve the first number in the sequence:

``` bash
./monotony -n my_awwesome_number
```

```
1
```

Repeatedly running the same command will display the next number in the sequence each time.


``` bash
./monotony -n my_awwesome_number
```

```
2
```

``` bash
./monotony -n my_awwesome_number
```

```
3
```

You can create as many of these sequences as you like:


``` bash
./monotony -n another_number ; ./monotony -n another_number
```

```
1
2
```

Since the current number is recorded in a config file (`~/.monotony.ini`), you can come back weeks later and continue the sequence exactly where you left off.

To reset a number, use `-r`:

``` bash
./monotony -r my_awesome_number
```

This removes the number from monotony completely.

To see a list of currently tracked numbers:

``` bash
./monotony -l
```

```
another_number : 2
example : 1
```

## License

Monotony is released under an MIT license. See LICENSE.md for more information.

