# BEREN Programming Language Interpreter

Welcome to **BEREN**, the Turkish-inspired programming language designed to make coding simple and intuitive! 🚀

This project is a Java-based interpreter for the BEREN language, featuring **lexical analysis** (Lexer) and **syntactic analysis** (Parser). Dive into the world of programming with clear syntax and powerful constructs like:
- 📊 **Variable declarations**
- ➕ **Arithmetic operations**
- 🔄 **Conditional statements (`if-else`)**
- 🔁 **Loop constructs (`while`)**

---

## 🛠 Features
- **Lexer**: Breaks down your code into meaningful units called tokens.
- **Parser**: Builds a structured **parse tree** to check program syntax.
- **BNF Grammar**: Defines the language rules for smooth interpretation.
- 🎯 **User-Friendly**: Simple syntax and error messages to guide you.

---

## 🚀 Getting Started

### Requirements
- **Java 8+** ✅
- A text file with BEREN code for testing 📄

### Running the Program
1. **Compile the program:**
   ```bash
   javac PL.java
   ```
2. **Run the program:**
   ```bash
   java PL
   ```
3. When prompted, enter the file number of your BEREN code (e.g., `1` for `sample1.txt`). Make sure your files are in the `src` directory!

---

## 🌟 Example Code
Here’s an example of BEREN code that demonstrates its simplicity:

```beren
sayi x = 5
ise (x > 3)
  x = x + 1
değilse
  x = x - 1
```

### Output
**Tokens:**
```
SAYI x =
NUMBER 5
IF ( x >
NUMBER 3
...
```

**Parse Tree (BNF Format):**
```
<program>
  <degiskenBildirimi>
  <ifDeyimi>
  ...
EOF
```

---

## 🌐 Language Grammar (BNF)
```
<program> ::= <degiskenBildirimi> <ifDeyimi> <whileDeyimi> EOF

<degiskenBildirimi> ::= SAYI ID ASSIGN NUMBER <degiskenBildirimi> | ε

<ifDeyimi> ::= IF LPAREN <kosul> RPAREN <ise> <değilse>

<ise> ::= <degiskenBildirimi>

<değilse> ::= ELSE <degiskenBildirimi>

<whileDeyimi> ::= WHILE LPAREN <kosul> RPAREN <dongu>

<dongu> ::= <atama> <dongu> | ε

<atama> ::= ID ASSIGN <ifade>

<ifade> ::= ID | ID PLUS NUMBER | ID MINUS NUMBER | ID MULTIPLY NUMBER | ID DIVIDE NUMBER

<kosul> ::= ID GREATER ID | ID LESS ID
```

---

## 🎨 File Structure
- `PL.java`: Main file containing Lexer and Parser.
- `src/sampleX.txt`: Test files for BEREN code.

---

## 🤝 Contributing
We welcome your contributions to enhance BEREN! 🛠 Feel free to:
- Submit issues
- Open pull requests

---

## 👨‍💻 Authors
- **Eren Yurtcu**  
- **Berkin Yıldırım**
