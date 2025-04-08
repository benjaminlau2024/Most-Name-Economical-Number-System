## 🔢 The Base System That Requires the Fewest Naming Symbols (0–1000 Integers)

> **Exercise:**  
> Consider the representation of integers in a positional numeral system with base \( a \). In order to name the numbers in this system, we need distinct words for the digits \( 0, 1, ..., a - 1 \), as well as for the powers of \( a \): \( a, a^2, a^3, \ldots \)
>
> How many different number words are needed to name all integers from 0 to 1000, for \( a = 2, 3, 4, \ldots, 15 \)?  
> Which base requires the fewest total number words?
>
> **Examples:**
>
> - If \( a = 10 \), we need 10 words for the digits (0–9), plus words for 10, 100, and 1000, totaling **13**.
> - If \( a = 20 \), we need 20 digit names (0–19), plus names for 20 and 400, totaling **22**.
> - If \( a = 100 \), we need 100 digit names and one unit (100), totaling **101**.

<small>This problem originates from the end of Chapter 1 of the book _What is Mathematics?_ by Richard Courant and Herbert Robbins.</small>

---

## 📊 Result Summary

After evaluating all bases from 2 to 15, we find that:

- ✅ **Base 4 requires the fewest total names: 8**
- For larger bases, the number of digit names grows too quickly, even though fewer power names are needed.

---

## 🧠 How It Works

The formula used to compute the number of names for a given base \( a \):

```text
number_of_words = number_of_digits + number_of_power_names
```

Where:

- `number_of_digits = a`
- `number_of_power_names = floor(log_a(1000)) + 1`

This accounts for all the symbols needed to name numbers from 0 to 1000.

---

## 🧪 Run the Code

### 🐍 Python

```bash
minimal_naming_units.py
```

### 💻 JavaScript (Node.js)

```bash
minimal_naming_units.js
```

You'll see the word count per base and which one minimizes the total.

---

## 📁 Files

- `minimal_base_name.py` — Python version
- `baseNameCalculator.js` — JavaScript version
- `README.md` — project introduction and usage

---

## 🏷️ Project Name

**English**: _The Base System That Requires the Fewest Naming Symbols (0–1000 Integers)_  
**中文**: _最省名称的转换进制系统（对于 0 – 1000 数字的表示）_

---

## 📚 Source

This project is based on an exercise from the classic mathematics book:

> Courant, R., & Robbins, H. _What is Mathematics?_ (Oxford University Press)

---

## 🙌 Author

Created by **Benjamin** (with help from **Lucy** ✨)

Feel free to ⭐ star or fork this repo if you found it interesting or useful!

---

## 📄 经典题目中文解释

> **问题**：  
> 考虑用 a 进制表示整数的情况，要给 0 到 1000 内的所有数字命名，需要给 a 的基本数字 (0 ~ a-1)和 a 的各级次方形式指定名称，即 $a^1$, $a^2$, $a^3$ 等等都需要有名字。
>
> **例如**：  
> 当 a = 10 时，我们需要有 10 个基本数字：0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 分别命名念作：零、一、二、三、四、五、六、七、八、九；还需要三种单位：$10^1$、$10^2$、$10^3$ 分别命名念作：十、百、千。
> <small>（其实是四个，还有一个$10^0$，只不过$10^0$这个单位是个位，不需要命名了，可以省略掉）</small>
>
> 这样 0-1000 以内任意数字都可以直接念出来。比如 374，念作：三百七十四;
> 本质上：374 = 3 &times; $10^2$ + 7 &times; $10^1$ + 4；其中 3 、$10^2$ 、7 、 $10^1$ 这四个数字或单位都有命名读音。
>
> 那么问题是，到底几进制是用最少的命名读音就可以念出 0-1000 之间的所有数字？
>
> **答案**：
> 名字的数量 = 基础数 + 单位数，就是 a + ⌊log_a(1000)⌋。根据对数运算法则，$log_{a}b$ 可进行变换。
> 当 a = 4 时，需要基本数字 0~3 ，与单位 $4^1$, $4^2$, $4^3$, $4^4$，总共 4 + 4 = 8 个，是所有进制中最省的。
