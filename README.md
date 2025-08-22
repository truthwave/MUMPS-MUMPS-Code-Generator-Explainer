<p align="center">
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

## 📸 **体験イメージ**
![デモ動画](https://github.com/TomoProgrammingDayori/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/%E8%B3%87%E6%96%99/%E3%83%87%E3%83%A2%E5%8B%95%E7%94%BB.gif)

![MUMPS言語の概要と特徴](https://github.com/TomoProgrammingDayori/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/%E8%B3%87%E6%96%99/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88/MUMPS%E8%A8%80%E8%AA%9E%E3%81%AE%E6%A6%82%E8%A6%81%E3%81%A8%E7%89%B9%E5%BE%B4.jpeg)

![MUMPSコード例（職員一覧表示）](https://github.com/TomoProgrammingDayori/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/%E8%B3%87%E6%96%99/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88/MUMPS%E3%82%B3%E3%83%BC%E3%83%89%E4%BE%8B%EF%BC%88%E8%81%B7%E5%93%A1%E4%B8%80%E8%A6%A7%E8%A1%A8%E7%A4%BA%EF%BC%89.jpeg)

![MUMPSコードの解説（職員一覧表示）](https://github.com/TomoProgrammingDayori/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/%E8%B3%87%E6%96%99/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88/MUMPS%E3%82%B3%E3%83%BC%E3%83%89%E3%81%AE%E8%A7%A3%E8%AA%AC%EF%BC%88%E8%81%B7%E5%93%A1%E4%B8%80%E8%A6%A7%E8%A1%A8%E7%A4%BA%EF%BC%89.jpeg)

![MUMPSコード例（日付表示）](https://github.com/TomoProgrammingDayori/MUMPS-MUMPS-Code-Generator-Explainer/blob/main/%E8%B3%87%E6%96%99/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88/MUMPS%E3%82%B3%E3%83%BC%E3%83%89%E4%BE%8B%EF%BC%88%E6%97%A5%E4%BB%98%E8%A1%A8%E7%A4%BA%EF%BC%89.jpeg)


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

## お気軽にご連絡ください
[📩 ご相談・お見積もりはこちら](mailto:realmadrid71214591@gmail.com)

---

## 📄 ライセンス / License

MIT License

---

> 「伝わらないコードは、無いのと同じ。」
>  ── MUMPSを、わかるものにしよう。

