# Mission 5 — Numbers and Data

## 1. Task / objective

Understand how computers represent numbers using decimal, binary and hexadecimal number systems. Practise converting values between these number systems manually, verify the results using Python, and build a small number converter.

The mission also introduces character encoding standards such as ASCII and UTF-8, which allow computers to represent and store text.

## 2. Work completed

### Task 5.1 — Convert numbers by hand

Converted the given values between decimal, binary and hexadecimal number systems.

**1. Decimal 13 to binary**

Repeatedly divide the decimal number by 2 and record the remainders.

| Division | Quotient | Remainder |
|---|---|---|
| 13 ÷ 2 | 6 | 1 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

Reading the remainders from bottom to top gives:

`13₁₀ = 1101₂`

**2. Decimal 25 to binary**

| Division | Quotient | Remainder |
|---|---|---|
| 25 ÷ 2 | 12 | 1 |
| 12 ÷ 2 | 6 | 0 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

Reading the remainders from bottom to top gives:

`25₁₀ = 11001₂`

**3. Binary 1010 to decimal**

Using positional values of powers of 2:

`1010₂ = (1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰)`

`= 8 + 0 + 2 + 0`

`= 10₁₀`

**4. Binary 1101 to decimal**

`1101₂ = (1 × 2³) + (1 × 2²) + (0 × 2¹) + (1 × 2⁰)`

`= 8 + 4 + 0 + 1`

`= 13₁₀`

**5. Hexadecimal A to decimal**

In hexadecimal, the digit A represents 10.

`A₁₆ = 10₁₀`

**6. Hexadecimal 1F to decimal**

In hexadecimal, F represents 15.

`1F₁₆ = (1 × 16¹) + (15 × 16⁰)`

`= 16 + 15`

`= 31₁₀`

**7. Binary 1111 to hexadecimal**

`1111₂ = 8 + 4 + 2 + 1 = 15₁₀`

The hexadecimal digit representing 15 is F.

`1111₂ = F₁₆`

### Task 5.2 — Verify using Python

Used Python's built-in conversion functions in the interactive environment to verify the manual calculations.

**Expressions and results:**

| Python expression | Result | Matches manual calculation |
|---|---|---|
| `bin(13)` | `'0b1101'` | Yes |
| `bin(25)` | `'0b11001'` | Yes |
| `int('1010', 2)` | `10` | Yes |
| `int('1101', 2)` | `13` | Yes |
| `hex(13)` | `'0xd'` | Yes |
| `hex(25)` | `'0x19'` | Yes |
| `int('A', 16)` | `10` | Yes |
| `int('1F', 16)` | `31` | Yes |
| `hex(int('1111', 2))` | `'0xf'` | Yes |

All the Python results matched the manual calculations.

Python's `bin()` and `hex()` functions include prefixes in their output: `0b` indicates binary, while `0x` indicates hexadecimal. The `int()` function can interpret a string using a specified base and return its decimal integer value.

### Task 5.3 — Build a small number converter

Created a Python program named `number_converter.py` that accepts a positive decimal integer and displays its binary and hexadecimal representations.

**Program:**

```python
number = int(input("Enter a positive decimal number: "))

print("Binary:", bin(number))
print("Hexadecimal:", hex(number))
```

**Execution command:**

```bash
python3 number_converter.py
```

**Test results:**

| Input | Binary output | Hexadecimal output |
|---|---|---|
| 10 | `0b1010` | `0xa` |
| 13 | `0b1101` | `0xd` |
| 25 | `0b11001` | `0x19` |

The program executed successfully for all three test values and displayed the correct conversions.

**Python functions used:**

- `input()` — Accepts the decimal number entered by the user as a string.
- `int()` — Converts the input string into an integer.
- `bin()` — Converts an integer into its binary representation.
- `hex()` — Converts an integer into its hexadecimal representation.

### Task 5.4 — How is text stored?

**ASCII decimal values:**

| Character | ASCII decimal value |
|---|---|
| Uppercase `A` | 65 |
| Lowercase `a` | 97 |

**Why does a computer need an encoding standard to store text?**

Computers store and process data as numerical values. An encoding standard provides an agreed mapping between characters and numbers, allowing different systems to store and interpret text consistently.

**Example of a character outside basic ASCII:**

The Indian Rupee symbol `₹` is not part of basic ASCII. UTF-8 supports a much wider range of characters and symbols, including this one.

## 3. Commands / tools used

| Command / Tool | Purpose |
|---|---|
| `cd mission-05-numbers-data` | Navigates into the Mission 5 directory. |
| `python3` | Opens the Python interactive environment. |
| `python3 number_converter.py` | Executes the number converter program. |
| `bin()` | Converts an integer into a binary string. |
| `hex()` | Converts an integer into a hexadecimal string. |
| `int(value, base)` | Converts a string representing a number in a specified base into an integer. |
| `input()` | Accepts input from the user. |
| `exit()` | Exits the Python interactive environment. |
| Terminal | Used to access Python and execute the converter program. |

## 4. My understanding

I learned how computers represent numbers using different number systems, particularly decimal, binary and hexadecimal.

Binary uses only two digits, 0 and 1, with each position representing a power of 2. Hexadecimal uses sixteen symbols, from 0 to 9 and A to F, making it a more compact way of representing binary values.

I also learned how to convert values between these number systems manually and verify the results using Python's built-in functions.

Building the number converter helped me understand how user input can be processed and converted into different representations using `int()`, `bin()` and `hex()`.

Another important concept was character encoding. Computers need encoding standards such as ASCII and UTF-8 to represent text as numerical data. ASCII covers a basic set of characters, while UTF-8 supports a much wider range of characters and symbols.

## 5. Difficulties faced

No major difficulties were encountered during the conversions or program execution.

One detail worth noting is that Python's `bin()` and `hex()` functions include prefixes (`0b` and `0x`) in their returned strings.

## 6. How I resolved them

Verified the conversion results using Python and compared them with the manual calculations. All the results matched successfully.

## 7. Evidence / files

- `number_converter.py` — Contains the Python program that converts a positive decimal integer into binary and hexadecimal representations.
- `README.md` — Contains the manual conversion calculations, Python verification results, converter details and explanations of character encoding.

## 8. Commit details

**Commit message:** `Build number converter and practise data representation`

**Push status:** Successfully committed and pushed to GitHub.
