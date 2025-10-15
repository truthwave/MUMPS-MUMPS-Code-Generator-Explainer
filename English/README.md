# MUMPS Code Generator & Explainer

> Read it. Fix it. Replace it.
> Legacy code can be neutralized through understanding.
> **Turn MUMPS back into an asset.**

<p align="center">
<img width="1536" height="1024" alt="MUMPS Code Generator" src="https://github.com/user-attachments/assets/b678caa6-0eb1-4e07-93f1-ca1de906d2b6" />

</p>

---

## Experience (Three Examples Sufficient)

- **Natural Language** → **MUMPS Generation**: Instructions in Japanese → Instant generation of standard MUMPS (with comments)
- **“Key Point Extraction” from Existing Code**: Break down global structures/loops/conditions in Japanese
- **Minimal Tutorial**: Focus on $ORDER scanning / Key differences in dialects (vs. ObjectScript)


---

## Before → After

- **Understanding existing code**: 60 minutes → **8 minutes**
- **Spec extraction iterations**: 3 times → **1 time**
- **Creating a replacement draft**: Blank → **Executable template**
> ※ Approximate. Varies based on code volume, naming, and data design.

---

## 📸Experience Image

![Demo](https://github.com/truthwave/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/English/Demo%20Movie.gif)

---

## 💻 Usage Examples

Below are prompts you can use as examples for GPT:

---

### ▶️ Input Example: Generating Code in Natural Language

```
Please create MUMPS code to store employee information in the global variable ^STAFF.
The fields are ID, Name, and Department.
```

---

### ✅ GPT Output Example

```mumps
; Example MUMPS code to store staff information
NEW ID,NAME,DEPT
SET ID=1001
SET NAME="Taro Yamada"
SET DEPT="General Affairs"

; Store in ^STAFF global
SET ^STAFF(ID,“NAME”)=NAME
SET ^STAFF(ID,“DEPT”)=DEPT
WRITE “Saved successfully”,!
```

---

### ▶️ Input Example (Existing Code Explanation)

```
^PATIENT(1234,“MED”)=250
What does this MUMPS code do?
```

---

### ✅ GPT Output Example

> ✅ Explanation:
>
> This code creates a subnode named “MED” within the global variable **^PATIENT**
> for patient ID “1234” and stores the value “250” there.
>
> **Possible meanings:**
>
> * Patient medical expenses
> * Medication dosage
> * Numerical data like blood pressure
>
> Actual meaning depends on system design.

---

### ▶️ Input Example (Grammar Question)

```
Please explain the difference between $O and $N.
```

---

### ✅ GPT Output Example

> ✅ Explanation:
>
> **\$O (Order)**
>
> * Retrieves the next key in a global or local array
> * Scans in forward order
>
> **\$N (Next)**
>
> * Often used with numeric indexes
> * Retrieves the next numeric index
>
> **Example:**
>
> ```mumps
> SET X=""
> FOR  SET X=$O(^DATA(X)) QUIT:X=“”  WRITE X,!
> ```
>
> → Since \$O can handle both strings and numbers, using \$O is now recommended over \$N.

---

## How to Use (3 Steps)

1. State your **purpose** (save/search/aggregate/replace) and **data model assumptions** in one line
2. Choose generate or explain (add summary or comments if needed)
3. **Verify** the output → **make minor adjustments**, then incorporate into documentation


---

## Technical Notes

- **Prompt Design**: Natural language → code / existing → key point extraction / comparison → replacement suggestions
- **Dialect Differences**: Note syntax differences between MUMPS and ObjectScript each time
- **Safety Measures**: Do not execute on production data (verify using **dump → stub**)

---

## Caution

- This tool is for **learning and reference purposes only**.
- Verify with **expert review/test environment** before actual deployment.
- Do not input real data or personal information.

---

## 🌐 Demo

[View MUMPS Code Generator & Explainer on ChatGPT](https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto)

---

## 📄 License

MIT License

---

## 🧑‍💻 Developer

**[Truth Wave ― 真理の波](https://github.com/truthwave)**  
Check out our portfolio and AI tool development information too!

## Feel Free to Contact Us
[📩 Inquiries & Quotes](mailto:realmadrid71214591@gmail.com)

---

## 🏁 In Closing

> **Don't embellish. Keep only the essentials.**
> That is the shortest path to turning legacy into an asset.
