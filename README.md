<p>

<img width="1536" height="1024" alt="古くて難しい MUMPS のコードも、もう怖くない。" src="https://github.com/user-attachments/assets/3f132036-c3f8-48d9-b081-43b70e88e86f" />

</p>

# MUMPS Code Generator & Explainer

「古くて難しいMUMPSのコードも、もう怖くない。」

---

## ✅ これができること（効能）
レガシーなMUMPSコードを、“理解しやすく” “保守しやすく”。
自然言語で指示するだけで、MUMPSコードを自動生成＆日本語でわかりやすく解説します。


---

## ⚙️ 主な機能 / Features

* ✅ **💡 自然言語 → MUMPSコード生成**

  * 日本語で指示を出すだけで、標準MUMPSコードを生成
  * コメント付きで、構文の意味を視覚化

* ✅ **🔍 既存MUMPSコードの読み解き支援**

  * グローバル構造、変数、ループ、条件分岐などを日本語で丁寧に解説
  * $O, $N, QUIT など独特な記法も言語化

* ✅ **📘 MUMPS文法のチュートリアル的解説**

  * 「MUMPS特有の動き」に絞った説明
  * 他の言語との違いを明示（ObjectScript との比較など）

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

### ▶️ 入力例：自然言語でコードを生成

```
職員情報をグローバル ^STAFF に保存する MUMPS コードを作ってください。
項目は ID、氏名、部署 です。
```

---

### ✅ GPT の出力例

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

### ▶️ 入力例（既存コードの解説）

```
^PATIENT(1234,"MED")=250
この MUMPS コードは何をしていますか？
```

---

### ✅ GPT の出力例

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

### ▶️ 入力例（文法の質問）

```
$O と $N の違いを教えてください。
```

---

### ✅ GPT の出力例

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

  * 自然言語からコード生成
  * 独自の構文対応プロンプト設計
  * ObjectScriptなどの方言との違いも明示
  * MUMPS学習用途としても活用可

---

## ⚠️ 注意事項 / Disclaimer

* 本ツールは学習・参考用です。
* 実際のシステム導入時は専門家によるレビューが必須です。
* 個人情報や実際の医療データは入力しないでください。

---

## 🌐 デモ / Demo

[ChatGPTで MUMPS Code Generator & Explainer を見る](https://chatgpt.com/g/g-686c88e3d0588191bee8d7cf3f755af7-mumpskotosheng-cheng-jie-shuo-asisutanto)

---

## 🧑‍💻  開発者

[ともプログラム便り](https://github.com/TomoProgrammingDayori)

ポートフォリオやAIツール開発に関する情報もぜひご覧ください！


---

## 📄 ライセンス / License

MIT License

---

> 「伝わらないコードは、無いのと同じ。」
>  ── MUMPSを、わかるものにしよう。

