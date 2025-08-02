# MUMPS Code Generator & Explainer

> **“No more fear of old and complex MUMPS code.”**

---

## 📌 Overview

**MUMPS Code Generator & Explainer** is a GPT-powered assistant designed to help developers and engineers **generate and understand MUMPS (M Language) code**, which is widely used in healthcare information systems and financial systems.

If you’ve ever thought:

- “I inherited legacy MUMPS code and don’t know where to start…”
- “I’m worried about making a mistake editing critical systems…”
- “I want to learn MUMPS but can’t find good examples…”

**This tool is for you.**

By generating clear examples and explanations, it helps **save time, reduce frustration, and give confidence** to both beginners and experienced engineers.

---

## ⚙️ Key Features

✅ **Automatic MUMPS Code Generation**
- Generates MUMPS code from natural language instructions
- Uses standard MUMPS syntax
- Adds comments to improve understanding

---

✅ **Explanation of Existing MUMPS Code**
- Explains logic, global structures, and variable meanings
- Focuses on key areas like globals, loops, and conditionals
- Explanations in Japanese (English coming soon)

---

✅ **Grammar and Syntax Guides**
- Clarifies differences between `$O` and `$N`
- Provides comparisons with other programming languages

---

✅ **Clear Distinction from Caché/ObjectScript**
- Highlights differences between standard MUMPS and proprietary Caché extensions

---

## 🎯 Target Users

- Developers maintaining healthcare IT (HIS) systems
- Engineers working on legacy financial systems
- Programmers learning MUMPS from scratch
- Technical professionals reviewing old codebases

---

## 💻 Usage Examples

Below are examples of what you can ask:

---

### 📥 Example Input (Natural Language → MUMPS Code)

```

Please create MUMPS code to store employee information in the ^STAFF global.
Fields: ID, Name, Department.

````

---

### ✅ Example Output

```mumps
; MUMPS code example to store employee information
NEW ID,NAME,DEPT
SET ID=1001
SET NAME="Taro Yamada"
SET DEPT="General Affairs"

; Store in ^STAFF global
SET ^STAFF(ID,"NAME")=NAME
SET ^STAFF(ID,"DEPT")=DEPT
WRITE "Data has been saved",!
````

---

### 📥 Example Input (Explain Existing Code)

```
^PATIENT(1234,"MED")=250
What does this MUMPS code do?
```

---

### ✅ Example Output

> **Explanation:**
>
> This line creates a sub-node in the global variable **^PATIENT**
> for patient ID “1234,” storing the value “250” under the “MED” node.
>
> **Possible meaning:**
>
> * Medical expenses
> * Dosage amount
> * Some numeric measurement
>
> The exact meaning depends on system context.

---

### 📥 Example Input (Grammar Question)

```
What’s the difference between $O and $N?
```

---

### ✅ Example Output

> **Explanation:**
>
> **\$O (Order):**
>
> * Retrieves the next key in a global or local array
> * Works with both string and numeric subscripts
>
> **\$N (Next):**
>
> * Mostly used with numeric indices
> * Returns the next numeric subscript
>
> **Example:**
>
> ```mumps
> SET X=""
> FOR  SET X=$O(^DATA(X)) QUIT:X=""  WRITE X,!
> ```
>
> In modern MUMPS code, `$O` is generally preferred over `$N`.

---

## 🛠 Technical Highlights

* **Custom Prompt Engineering**

  * Tailored for MUMPS’ unique syntax and globals
  * Always includes helpful comments

* **Clear Differentiation**

  * Explains differences between standard MUMPS and Caché/ObjectScript

* **Safety Considerations**

  * Warns against entering personal or real medical data
  * Emphasizes reviewing generated code before production use

* **Learning-Oriented**

  * Designed to serve as a learning and reference tool

---

## ⚠️ Disclaimer

* This tool is intended for **learning and reference only**.
* Always have real implementations reviewed by qualified professionals.
* Do not input personal or confidential medical data.

---

## 🌐 Demo

[Try MUMPS Code Generator & Explainer on ChatGPT](https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto)

---

## 👨‍💻 My Role

I handled all aspects of this project:

* Prompt engineering optimized for MUMPS syntax
* UX design for clarity and ease of use
* Testing and refinement to improve explanation quality

---

## 📄 License

MIT License

---

> **“Old MUMPS code doesn’t have to be scary anymore.”*

---
