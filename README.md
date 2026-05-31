# CuneiScript
A programming language created by Google Gemini that uses Sumerian Language.

Designing a programming language based on Sumerian is a brilliant concept. Because Sumerian is an **agglutinative language** (where prefixes and suffixes are glued onto a root word to change its meaning) and relies heavily on **determinatives** (silent markers that classify words), it translates beautifully into a strongly-typed, object-oriented, or functional programming paradigm.

Let's call this esoteric programming language **CuneiScript** (or simply **EME-GIR**).

Here is the architectural blueprint for how Sumerian grammar translates into code syntax.

---

## 1. Core Language Mechanics

### Determinatives as Data Types (The Silent Typers)

In written Sumerian, a silent sign was placed before a word to tell the reader what category it belonged to (e.g., `{d}` for gods, `{giš}` for wood/tools). In EME-GIR, these act as strict variable type declarations.

| Sumerian Determinative | Meaning in History | EME-GIR Data Type |
| --- | --- | --- |
| `{d}` (*Dingir*) | Divine / God | **Constant / Immutable** |
| `{lu}` (*Lu*) | Person / Man | **Object / Class Instance** |
| `{šam}` (*Šam*) | Plant / Herb | **Array / List (Growth)** |
| `{im}` (*Im*) | Clay / Tablet | **String / Text** |
| `{ninda}` (*Ninda*) | Bread / Food | **Number / Integer / Float** |

### Agglutinative Syntax (Chaining Methods)

Instead of writing nested functions like `print(uppercase(reverse(text)))`, EME-GIR chains prefixes and suffixes to a root verb. The root verb always comes at the **very end** of the statement (Sumerian is a Subject-Object-Verb language).

---

## 2. Basic Syntax & Operators

### Variable Declaration

To declare a variable, you state the type determinative, the identifier, the assignment operator (`=ba` - *to bestow/give*), and the value.

```
{ninda} ku_3 =ba 42; 
// Type: Number | Name: ku_3 (silver) | Assigns: 42
// Meaning: Let the silver equal 42 pieces of bread.

{im} mu =ba "Silim-ma!"; 
// Type: String | Name: mu (name/line) | Assigns: "Hello!"

```

### Conditionals (`tukum-bi` / If)

In Sumerian, `tukum-bi` means "if."

```
tukum-bi (ku_3 > 40) {
    // Code executes if true
}

```

### Loops (`u_4-da` / While / As long as)

`U4-da` literally means "on the day when" or "whenever."

```
{ninda} i =ba 0;

u_4-da (i < 10) {
    // Loop body
    i =ba i + 1;
}

```

---

## 3. The Ultimate Root Verb: Chaining Functions

Sumerian verbs are incredibly complex, packing subject, object, direction, and tense into one word via prefixes and suffixes. In EME-GIR, functions are executed by modifying a root verb.

Let's look at the root verb **`ĝar`** (to place / to output / to write).

* `i-` : System prefix (activates the console).
* `-b-` : Inanimate object pronoun infix (it).
* `-ĝar` : The root verb (to place).
* `-e` : Terminative suffix (execute / command line break).

Therefore, the command to print to the console is **`ibĝare`**.

```
{im} ki =ba "Hello, World!";
ki.ibĝare; 
// Outputs: Hello, World!

```

If you want to append text to a file, you change the directive prefix to **`bi-`** (into it):

```
ki.bibĝare; 
// Appends "Hello, World!" into the database/file

```

---

## 4. A Complete Script Example: The Barley Ledger

Let’s write a functional program in EME-GIR that calculates the tax on a harvest of barley (`še`). If the barley harvest is greater than 100 bushels, a 10% tax is deducted for the temple of Enlil.

```
// Define a Constant for the Temple of the Storm God
{d}ENLIL =ba "Temple Account";

// Declare harvest amount (Number)
{ninda} še =ba 150;
{ninda} ibila_tax =ba 0;

// Conditional Logic
tukum-bi (še > 100) {
    // 10% math
    ibila_tax =ba še * 0.10;
    še =ba še - ibila_tax;
}

// Format the output string using agglutination
{im} report =ba "Tax collected for " + {d}ENLIL + ": " + ibila_tax;

// Output to console
report.ibĝare;

```

---

## 5. Standard Error Handling

When code crashes in EME-GIR, it doesn't give you a boring stack trace. It returns a historical tablet omen.

* **`HUL` (Null Pointer Exception):** *An evil omen. The foundations of the temple are shaken.*
* **`BALA` (Infinite Loop / Overflow):** *Rebellion. The reign of the current dynasty has overstepped its years.*
* **`NU-ZU` (Syntax Error):** *Unknown sign. The apprentice scribe has dropped clay on the tablet.*
