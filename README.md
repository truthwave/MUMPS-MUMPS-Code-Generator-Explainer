# MUMPS Code Generator & Explainer

> “No more fear of old and complex MUMPS code.”

---

## 📌 Overview

**MUMPS Code Generator & Explainer** is a GPT-powered assistant designed to help developers and engineers generate and understand MUMPS (M Language) code, widely used in healthcare information systems and financial systems.

It’s perfect for:

- Developers struggling to read legacy MUMPS code
- Engineers maintaining systems they didn’t originally build
- Beginners who want to learn MUMPS from scratch

This tool **saves time, reduces frustration, and helps both beginners and legacy system engineers confidently work with MUMPS.**

---

## ⚙️ Key Features

- ✅ **Automatic MUMPS Code Generation**
  - Generates MUMPS code from natural language instructions
  - Uses standard MUMPS syntax
  - Adds comments to improve understanding

- ✅ **Explanation of Existing MUMPS Code**
  - Explains code logic, global structures, and variable meanings
  - Focuses on globals, loops, conditionals, and other key concepts
  - Explanations available in Japanese (English coming soon)

- ✅ **Grammar and Syntax Guides**
  - Clarifies differences between `$O` and `$N`
  - Provides comparisons with other languages

- ✅ **Clear Distinction from Caché/ObjectScript**
  - Explains differences between standard MUMPS and proprietary Caché extensions

---

## 🎯 Target Users

- Developers or maintainers in healthcare IT (HIS)
- Engineers working on legacy financial systems
- Programmers new to MUMPS
- Technical professionals wanting to learn MUMPS fundamentals

---

## 💻 Usage Examples

Below are example prompts you can ask the GPT:

---

### Example Input (Natural Language → MUMPS Code Generation)

```

Please create MUMPS code to store employee information in the ^STAFF global.
Fields: ID, Name, Department.

````

---

### GPT Example Output

```mumps
; Example MUMPS code to store employee information
NEW ID,NAME,DEPT
SET ID=1001
SET NAME="Taro Yamada"
SET DEPT="General Affairs"

; Save to ^STAFF global
SET ^STAFF(ID,"NAME")=NAME
SET ^STAFF(ID,"DEPT")=DEPT
WRITE "Data has been saved",!
````

---

### Example Input (Explaining Existing Code)

```
^PATIENT(1234,"MED")=250
What does this MUMPS code do?
```

---

### GPT Example Output

> ✅ Explanation:
>
> This line creates a sub-node under the global variable **^PATIENT**
> for patient ID “1234,” storing the value “250” under the “MED” node.
>
> **Possible meanings:**
>
> * Medical expenses
> * Dosage amount
> * Numeric data like blood pressure
>
> The exact meaning depends on the system’s design.

---

### Example Input (Grammar Question)

```
What’s the difference between $O and $N in MUMPS?
```

---

### GPT Example Output

> ✅ Explanation:
>
> **\$O (Order)**
>
> * Retrieves the next key in a global or local array
> * Traverses in ascending order
>
> **\$N (Next)**
>
> * Often used with numeric subscripts
> * Retrieves the next numeric index
>
> **Example:**
>
> ```mumps
> SET X=""
> FOR  SET X=$O(^DATA(X)) QUIT:X=""  WRITE X,!
> ```
>
> → `$O` handles both numeric and string subscripts and is generally preferred in modern MUMPS code.

---

## 🛠 Technical Highlights

* **Custom Prompt Engineering**

  * Tailored prompts for MUMPS’ unique syntax and global data structures
  * Always includes explanatory comments for better understanding

* **Clear Differentiation from Caché/ObjectScript**

  * Explicitly explains differences between standard MUMPS and proprietary extensions

* **Safety Considerations**

  * Warns users not to enter personal or real medical data
  * Emphasizes that generated code should be reviewed before production use

* **Learning-Oriented Design**

  * Doubles as a training tool for learning MUMPS

---

## ⚠️ Disclaimer

* This tool is intended for learning and reference only.
* Always have real system implementations reviewed by experts before deploying code.
* Do not input personal or confidential medical data.

---

## 🌐 Demo

[View MUMPS Code Generator & Explainer on ChatGPT](https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto)

---

## 👨‍💻 My Role

I designed and developed this GPT, including:

* Prompt engineering focused on MUMPS syntax
* UX design to simplify interaction
* Testing and refining explanations for clarity

---

## 📄 License

MIT License

---

---

# MUMPS Code Generator & Explainer

「古くて難しいMUMPSのコードも、もう怖くない。」

---

## 📌 概要 / Overview

**MUMPS Code Generator & Explainer** は、医療情報システムや金融システムなどで使われる
MUMPS（M言語）のコード生成と解説を支援する GPT アシスタントです。

以下のような方に最適です：

* 昔書いた MUMPS のコードが読めない方
* 保守を引き継いだが理解に苦しんでいる方
* MUMPS を基礎から学びたい方

このツールにより **作業時間短縮・理解促進・レガシー保守の不安軽減** が可能になります。

---

## ⚙️ 主な機能 / Features

* ✅ **MUMPSコード自動生成**

  * 自然言語の指示から MUMPS コードを生成
  * 標準的な構文を用いて出力
  * コメントを付加し理解を助ける

* ✅ **既存 MUMPS コードの解説**

  * 提示されたコードの構造や変数の意味を日本語で解説
  * グローバル変数やループ構造、条件分岐などにフォーカス
  * 英語での解説は今後対応予定

* ✅ **文法・構文の解説**

  * \$O と \$N の違いなど、よくある疑問を解説
  * 他のプログラミング言語との比較も提供

* ✅ **Caché/ObjectScript との違いを明示**

  * 標準MUMPS構文と独自拡張との違いを説明

---

## 🎯 想定ユーザー / Target Users

* 医療情報システム（HIS）の開発者・保守担当者
* 金融系レガシーシステムの保守エンジニア
* MUMPS初学者
* MUMPSの基礎を学びたい技術者

---

## 💻 使用例 / Usage Examples

以下は GPT への例として使えるプロンプトです：

---

### 入力例（自然言語 → MUMPSコード生成）

```
職員情報をグローバル ^STAFF に保存する MUMPS コードを作ってください。
項目は ID、氏名、部署 です。
```

---

### GPT の出力例

```mumps
; 職員情報を保存する MUMPS コード例
NEW ID,NAME,DEPT
SET ID=1001
SET NAME="山田太郎"
SET DEPT="総務"

; ^STAFF グローバルに保存
SET ^STAFF(ID,"NAME")=NAME
SET ^STAFF(ID,"DEPT")=DEPT
WRITE "保存が完了しました",!
```

---

### 入力例（既存コードの解説）

```
^PATIENT(1234,"MED")=250
この MUMPS コードは何をしていますか？
```

---

### GPT の出力例

> ✅ 解説：
>
> このコードは、グローバル変数 **^PATIENT** の中に
> 患者ID「1234」の MED というサブノードを作成し、
> そこに「250」という値を格納しています。
>
> **想定される意味：**
>
> * 患者の医療費
> * 投薬量
> * 血圧などの数値データ
>
> 実際の意味はシステム設計によります。

---

### 入力例（文法の質問）

```
$O と $N の違いを教えてください。
```

---

### GPT の出力例

> ✅ 解説：
>
> **\$O（Order）**
>
> * グローバルやローカル配列の次のキーを取得
> * 順方向に走査
>
> **\$N（Next）**
>
> * 数値のインデックスに対して使うことが多い
> * 次の数値インデックスを取得
>
> **例：**
>
> ```mumps
> SET X=""
> FOR  SET X=$O(^DATA(X)) QUIT:X=""  WRITE X,!
> ```
>
> → \$O は文字列も数値も扱えるため、近年は \$N より \$O の使用が推奨されています。

---

## 🛠 技術的ポイント / Technical Highlights

* **カスタムプロンプト設計**

  * MUMPS の独特な構文やグローバル構造を扱うための最適化
  * 初学者でも理解しやすい解説を自動付与

* **Caché/ObjectScript との違いを明示**

  * 標準構文と独自拡張の差を明確に説明

* **安全設計**

  * 個人情報や医療データの入力を避けるよう注意喚起
  * コードは例であり、実装前に必ず確認する旨を伝達

* **学習支援機能**

  * コード生成だけでなく、学習ツールとしても活用可能

---

## ⚠️ 注意事項 / Disclaimer

* 本ツールは学習・参考用です。
* 実際のシステム導入時は専門家によるレビューが必須です。
* 個人情報や実際の医療データは入力しないでください。

---

## 🌐 デモ / Demo

[ChatGPTで MUMPS Code Generator & Explainer を見る](https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto)

---

## 👨‍💻 開発者 / My Role

本ツールの以下を全て担当しました：

* MUMPS構文に特化したプロンプト設計
* 操作を簡単にするUX設計
* 出力精度と解説内容のブラッシュアップ

---

## 📄 ライセンス / License

MIT License

---

> 「古くて難しい MUMPS のコードも、もう怖くない。」

```
