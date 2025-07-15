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

> **“Old MUMPS code doesn’t have to be scary anymore.”**

```

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
