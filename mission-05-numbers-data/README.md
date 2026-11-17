# Mission 5 - Numbers and data

## 1. Task / objective

Convert between decimal, binary and hexadecimal with working, check the answers in Python, make a small converter and look at text encoding.

## 2. Work completed

### Manual conversions

| Question | Working and answer |
| --- | --- |
| Decimal 13 to binary | Divide by 2: `13 = 2(6) + 1`, `6 = 2(3) + 0`, `3 = 2(1) + 1`, `1 = 2(0) + 1`. Read the remainders from bottom to top: **1101₂**. |
| Decimal 25 to binary | `25 = 2(12) + 1`, `12 = 2(6) + 0`, `6 = 2(3) + 0`, `3 = 2(1) + 1`, `1 = 2(0) + 1`. Read bottom to top: **11001₂**. |
| Binary 1010 to decimal | `1×2³ + 0×2² + 1×2¹ + 0×2⁰ = 8 + 0 + 2 + 0 =` **10₁₀**. |
| Binary 1101 to decimal | `1×2³ + 1×2² + 0×2¹ + 1×2⁰ = 8 + 4 + 0 + 1 =` **13₁₀**. |
| Hexadecimal A to decimal | `A = 10`, so `10×16⁰ =` **10₁₀**. |
| Hexadecimal 1F to decimal | `F = 15`, so `1×16¹ + 15×16⁰ = 16 + 15 =` **31₁₀**. |
| Binary 1111 to hexadecimal | One group of four bits: `1×8 + 1×4 + 1×2 + 1×1 = 15`. Hexadecimal digit 15 is **F₁₆**. |

### Python verification

I opened the Python 3 interactive prompt and checked the calculations. The `0b` prefix means binary and the `0x` prefix means hexadecimal.

| Expression tested | Python result | Matches the manual answer? |
| --- | --- | --- |
| `bin(13)` | `0b1101` | Yes |
| `bin(25)` | `0b11001` | Yes |
| `int('1010', 2)` | `10` | Yes |
| `int('1101', 2)` | `13` | Yes |
| `int('A', 16)` | `10` | Yes |
| `int('1F', 16)` | `31` | Yes |
| `hex(int('1111', 2))` | `0xf` | Yes |
| `hex(10)` | `0xa` | Yes, it is the reverse check for A |
| `hex(31)` | `0x1f` | Yes, it is the reverse check for 1F |

### Number converter

I created `number_converter.py`, which asks for a positive decimal number and prints its binary and hexadecimal forms. I tested it from Terminal:

| Decimal input | Binary output | Hexadecimal output |
| --- | --- | --- |
| 13 | `0b1101` | `0xd` |
| 25 | `0b11001` | `0x19` |
| 31 | `0b11111` | `0x1f` |

### Text encoding

`ord('A')` returned **65** and `ord('a')` returned **97**, their ASCII decimal codes.

A computer needs an encoding standard to match characters with the numbers or bytes it stores, so the text can be read back properly. The rupee symbol `₹` is not part of basic ASCII, but UTF-8 can represent it.

## 3. Commands / tools used

| Command or function | Purpose |
| --- | --- |
| `python3 -q` | Open the Python interactive prompt for verification. |
| `bin()` | Convert an integer to a binary string. |
| `hex()` | Convert an integer to a hexadecimal string. |
| `int(text, base)` | Read binary or hexadecimal text as an integer. |
| `ord()` | Check the numeric code for a character. |
| `python3 number_converter.py` | Run the converter with test inputs. |
| `git add`, `git commit`, `git push` | Stage, save and publish this mission. |

## 4. My understanding

In `number_converter.py`, `input()` grabs the text I type. `int()` turns that text into an actual integer so the program can work with it. Then `bin()` and `hex()` take the integer and convert it into binary and hexadecimal strings, and `print()` shows those results.

For the manual work, I used repeated division by 2 to turn decimal numbers into binary and read the remainders from bottom to top. For binary to decimal, I added the value of each bit's position. Hexadecimal uses 16 as its base, so `F` has the value 15.

## 5. Difficulties faced

No major difficulty.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

This README shows the manual steps, Python checks and three converter tests. The working program is `number_converter.py`.

## 8. Commit details

Commit message: `Build number converter and practise data representation`. Pushed to GitHub on the `main` branch.
