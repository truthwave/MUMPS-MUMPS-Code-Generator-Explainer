# MUMPS Code Generator & Explainer

> “No more fear of old and complex MUMPS code.”

---

## 📌 Overview

**MUMPS Code Generator & Explainer** is a GPT-powered assistant that helps generate and explain MUMPS (M Language) code, commonly used in medical information systems and financial systems.

It’s designed for anyone who:

- Struggles to read old MUMPS code they wrote years ago
- Has inherited system maintenance but can’t understand the code
- Wants to learn MUMPS from scratch

This tool is suitable for both beginners and engineers maintaining legacy systems.

---

## ⚙️ Features

✅ **Automatic MUMPS Code Generation**

- Generates MUMPS code based on natural language instructions
- Outputs standard MUMPS syntax
- Includes comments for better understanding

✅ **Explanation of Existing MUMPS Code**

- Explains code structure and variables in plain Japanese (or English in future updates)
- Focuses on global variables, loops, conditionals, and other key concepts

✅ **Grammar and Syntax Guides**

- Answers common questions like the difference between `$O` and `$N`
- Provides comparisons with other programming languages

✅ **Clarifies Differences with Caché/ObjectScript**

- Explains differences between standard MUMPS syntax and proprietary extensions in Caché

---

## 🎯 Target Users

- Developers or maintenance engineers in healthcare information systems (HIS)
- Engineers maintaining legacy financial systems
- Programmers new to MUMPS
- Technical professionals looking to learn MUMPS fundamentals

---

## 💻 Usage Examples

### Example Input (Natural Language → MUMPS Code Generation)



```markdown
# MUMPS Code Generator & Explainer

「古くて難しいMUMPSのコードも、もう怖くない。」

---

## 概要 / Overview

**MUMPS Code Generator & Explainer** は、医療情報システムや金融システムなどで使われる  
MUMPS（M言語）のコード生成と解説を支援する GPT アシスタントです。

「昔書いた MUMPS のコードが読めない」  
「保守を引き継いだけど理解できない」  
「MUMPS をゼロから学びたい」

そんな悩みに対応し、MUMPS 初心者からレガシー保守担当者まで幅広く活用いただけます。

---

## 主な機能 / Features

✅ **MUMPSコード自動生成**

- ユーザーの自然言語の指示をもとに
- 標準的な MUMPS 構文でコードを出力
- コメント付きで理解を助ける

✅ **既存 MUMPS コードの解説**

- 提示されたコードの構造や変数の意味を日本語で説明
- グローバル変数の構造やループ処理、条件分岐などに重点

✅ **MUMPS の文法解説**

- $O と $N の違いなど、よくある疑問に具体例で回答
- 他のプログラミング言語との比較も交えて解説

✅ **Caché/ObjectScript との違いを明示**

- MUMPS 固有の構文と Caché 独自拡張の差異を解説

---

## 想定ユーザー / Target Users

- 医療情報システム（HIS）の開発者や保守担当者
- 金融システムのレガシー保守を担当するエンジニア
- MUMPS に初めて触れるプログラマー
- MUMPS の基礎を学びたい技術者

---

## 使用例 / Usage Examples

### 入力例（自然言語 → MUMPSコード生成）

```

職員情報をグローバル ^STAFF に保存する MUMPS コードを作ってください。
項目は ID、氏名、部署 です。

````

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
````

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
> 患者 ID「1234」の MED というサブノードを作り、
> その値として「250」を格納しています。
>
> **想定される意味：**
>
> * 患者の医療費
> * 投薬量
> * 血圧などの数値データ
>
> どんな意味を持たせるかはシステム設計によります。

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
> * 数字の次のインデックスを取得
>
> **例：**
>
> ```mumps
> SET X=""
> FOR  SET X=$O(^DATA(X)) QUIT:X=""  WRITE X,!
> ```
>
> → \$O は文字列や数値どちらも扱えるが、
> 最近では \$N より \$O が推奨されることが多いです。

---

## 技術的ポイント / Technical Highlights

* **カスタムプロンプト設計**

  * MUMPS の独特な構文やグローバル変数構造を的確に取り扱うようプロンプトを最適化
  * 初心者でも理解できるよう、必ずコメントや解説を付加

* **Caché/ObjectScript との違いを明確化**

  * MUMPS の純粋構文と、Caché 独自拡張を明示的に区別

* **安全性への配慮**

  * 個人情報や医療データを生成・解説しないよう注意喚起
  * 「このコードは例であり、導入前に必ず確認を」とユーザーに伝える

* **学習支援に特化**

  * 単なるコード生成に留まらず、MUMPS の知識習得ツールとしても活用可能

---

## 注意事項 / Disclaimer

* 本ツールは MUMPS の学習および参考情報提供を目的としています。
* 実際のシステム導入・保守にあたっては、必ず専門家のレビューを受けてください。
* 個人情報や実データは入力しないでください。

---

## 今後の展望 / Future Plans

* 英語版の出力精度向上
* 医療システムにおける具体的なユースケース解説機能
* グローバル構造ビジュアライザーとの連携
* よくあるエラーコードの解説機能

---

## ライセンス / License

MIT License

---

「古くて難しい MUMPS のコードも、もう怖くない。」

→https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto
