# Powers of 2
Let's explore the world of **powers of 2**. 



Powers of two when used as a base 2 numbering system is also called **binary**.



1. **Positive Powers of Two**:
   - These include values like $$2^1 = 2$$, $$2^2 = 4$$, $$2^3 = 8$$, and so on.
   - They play a crucial role in binary numerals, computer science, and digital systems.
2. **Negative Powers of Two**:
   - These involve fractions like $$2^{-1} = \frac{1}{2}$$, $$2^{-2} = \frac{1}{4}$$, and $$2^{-3} = \frac{1}{8}$$.
   - They're essential for understanding decimal to binary conversion.
3. **Nonnegative Powers of Two**:
   - These cover both positive and zero exponents (e.g., $$2^0 = 1$$).
   - They appear in various mathematical contexts.



## A Little Computer Science

In computer science one bit is always reserved for sign ( + / - ). Unless it is marked as `unsigned`. Ergo, `256` may be the 8th power of two but an 8 bit integer has a limit of `2^8-1= 127`. C integers have a positive limit of`32767`.

>   -2^(n - 1) to 2^(n - 1) - 1. As you can see, the upper bound gets a -1 that the lower bound doesn't. — [Stack Overflow](https://stackoverflow.com/questions/18558271/why-the-range-of-int-is-32768-to-32767)

In computing, a byte is most commonly made up of 8 bits

`1111 1111` =  `255` so `1 byte`  is `0 - 255`

A hexedecimal (base 16 number system)  uses two values to reach the `255` bit range (`0xFF` = `255` = `11111111`).

## Some Powers of Two

*Committing exponents `0` - `10` to memory is a good start*

$$2^0 = 1$$

$$2^1 = 2$$

$$2^2 = 4$$

$$2^3 = 8$$

$$2^4 = 16$$

$$2^5 = 32$$

$$2^6 = 64$$

$$2^7 = 128$$

$$2^8 = 256$$



---

$$2^9 = 512$$

$$2^{10} = 1024$$

$$2^{11} = 2048$$

$$2^{12} = 4096$$

$$2^{13} = 8192$$

$$2^{14} = 16384$$

$$2^{15} = 32768$$

$$2^{16} = 65536$$



---

$$2^{17} = 131072$$

$$2^{18} = 262144$$

$$2^{19} = 524288$$

$$2^{20} = 1048576$$

$$2^{21} = 2097152$$

$$2^{22} = 4194304$$

$$2^{23} = 8388608$$

$$2^{24} = 16777216$$

$$2^{25} = 33554432$$

$$2^{26} = 67108864$$

$$2^{27} = 134217728$$

$$2^{28} = 268435456$$

$$2^{29} = 536870912$$

$$2^{30} = 1073741824$$

$$2^{31} = 2147483648$$

$$2^{32} = 4294967296$$

---

## More Computer Science

```js
let maxSafeInteger = Number.MAX_SAFE_INTEGER;
console.log(maxSafeInteger); // Outputs: 9007199254740991
```

This limit is due to the way numbers are represented in JavaScript, which uses double-precision floating-point format. This format allocates 52 bits to represent the mantissa, allowing it to safely represent integers up to $$2^{53−1}$$

For numbers beyond this range, **JavaScript** provides the `BigInt` type, which can represent integers of arbitrary size.

----

In **Godot Engine**, the limit for an `integer` is based on a signed 64-bit integer type. This means it can take values from 
$$−2^{63}$$
 to 
 $$2^{63−1}$$

Which is from `-9223372036854775808` to `9223372036854775807`.