<!-- @format -->

# Chapter 2: Basic Components

- 0/1, low/high, false/true, and deasserted/asserted

## 2.1

- Chisel provides three data types to describe connections, combinational logic, and
  registers:

1. Bits
2. UInt,
3. SInt.

- UInt and SInt extend Bits, and all three types represent a vector of bits

Here is the definition for different types, an 8-bit Bits, an 8-bit unsigned integer, and a 10-bit signed integer:

- Bits (8.W)
- UInt (8.W)
- SInt (10. W)

- The width of a vector of bits is defined by a Chisel width type (Width)

Defining constants by using a Scala integer and converting it to a Chisel type:
0.U // defines a UInt constant of 0
-3.S // defines a SInt constant of -3

Constants can also be defined with a width, by using the Chisel width type:
3.U(4.W) // An 4-bit constant of 3

- Bool
  Bool ()
  true .B
  false .B

## 2.2 Combinational Circuits

The following line of code defines a circuit that combines signals a and b with and gates and combines the result with signal c with or gates and names it logic.

```scala
val logic = (a & b) | c
```

**Standard Logical Operations:**

1. val and = a & b // bitwise and
2. val or = a | b // bitwise or
3. val xor = a ˆ b // bitwise xor
4. val not = ˜a // bitwise negation

**Arithematic Operations:**

1. val add = a + b // addition
2. val sub = a - b // subtraction
3. val neg = -a // negate
4. val mul = a \* b // multiplication
5. val div = a / b // division
6. val mod = a % b // modulo operation
