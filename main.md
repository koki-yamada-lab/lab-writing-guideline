---
marp: true
paginate: true
theme: default
size: 16:9
transition: "none"
style: |
    section {
        justify-content: start;
        font-size: 22px;
    }
    section.title{
        justify-content: center;
        text-align: center;
        font-size: 29px;
    }
---

<!-- コメント：画像を中央に配置する centerコマンドを有効に -->
<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

<!--_class: title-->

# 研究室の論文執筆ガイドライン 

(2026年7月作成)

東京農工大学大学院先進学際科学府
山田宏樹

---

# ガイドライン作成の意図

## 論文執筆は非常に難しい！

- 体裁・フォーマットに関してルールが多い
- 研究をわかりやすく伝えるのがそもそも難しい
- 論理構成・ストーリーを考えるのに，研究に関しての深い理解が必要

## 最低限必要な知識を身につけてから論文執筆をしましょう

### 体裁・フォーマットに関するルール

このルールが遵守されていないと，読者は論文の内容の真偽に疑念を持ちます．
まずは，このルールを把握し，ルールを遵守することが重要です．


### アカデミックライティングの基礎

アカデミックライティングを学ぶことで，論文の論理構成に関する型を知ることができます，この型を知れば，論文執筆の手がかりになります．

---

# 想定する聴衆

## まだ論文執筆に慣れていない情報系の学生がメインターゲット

- 論文執筆は分野によってフォーマットも異なりますし，好まれる論理構成の型も結構違いがあります．
- 今回は，情報系がメインターゲットですが，同じ情報系の中でも，信号処理分野，機械学習分野，Computer Vision分野などでも微妙に違いがあるので注意しましょう．
- この資料や参考文献に書いてある内容を鵜呑みにしすぎないようにしましょう．内容に違和感があったら，自身が取り組んでいる研究がよく載っている論文誌ではどうなっているかを自分で確認しましょう．

---

# 目次

## [論文の体裁・フォーマットに関するルール](#論文の体裁・フォーマットに関するルール)

- チェックリスト，LaTeX・数式・参考文献のルール

## [アカデミックライティングの基礎を学ぶ](#アカデミックライティングの基礎を学ぶ-1)

- 文を正しく書く技術
- 論理構成・ストーリー構成

## [研究室の論文執筆の流れ](#研究室の論文執筆の流れ-1)


---

# 論文の体裁・フォーマットに関するルール

---

# 体裁・フォーマット

論文を書き始めた学生がまず意識すべきことは，論文の体裁・フォーマットのルールを守るということです．こういった**ルールを知っていれば機械的に修正できることを，他人に添削させないようにしましょう**．人に添削をお願いするときには，このルールが守れているかを事前に確認しましょう．

## 体裁・フォーマットに関するチェックリストを作りました

思いつくものを一通りチェックリストに入れました．初めて論文を書く人は注意深くこのチェックリストを読み，ルールを遵守するようにしてください．特に注意が必要な項目についてこれから説明しますが，これらはチェックリストのごく一部なので，チェックリストは別で熟読してください．


---

# LaTeXに関するルール

本研究室では，LaTeXを使って論文を書きます．LaTeXを正しく使うことで，体裁・フォーマットのルールを遵守しやすくなります．

## まずはこれらの記事を読もう！

**以下の記事は全部読んでおいてください**．これらの記事を参考にチェックリストを作っているので，なぜこういったチェックが必要なのかを記事を読むことで理解しましょう．

- [LaTeXにおける正しい論文の書き方](https://qiita.com/birdwatcher/items/5ec42b35d84d3ee2ffbb)
- [アカデミックヤクザにキレられないためのLaTeX論文執筆メソッド](https://qiita.com/suigin/items/10960e516f2d44f6b6de)
- [イショティハドゥスにキレられないためのLaTeX論文執筆メソッド](https://qiita.com/Ishotihadus/items/bbbb85f54e6a4e7aaac0)


---

# 数式に関するルール
 
### 変数の書体を論文内で統一しましょう．以下の表はあくまで一例なので，分野の慣習に従うようにしてください．


| 対象         | LaTeXでの表記                                   | 表示例                                 | 基本的な規則・使用例           |
| ---------- | ------------------------------------------- | ----------------------------------- | -------------------- |
| スカラー       | `x`, `a`, `\lambda`                   | $x,\ a,\ \lambda$                   | 小文字のイタリック体           |
| ベクトル       | `\boldsymbol{x}`                              | $\boldsymbol{x}$                            | 小文字の太字               |
| 行列         | `\boldsymbol{A}`                              | $\boldsymbol{A}$                            | 大文字の太字               |
| 関数         | `f`, `g`                              | $f,\ g$                             | 通常は小文字のイタリック体        |
| 集合         | `\mathcal{S}`                         | $\mathcal{S}$                       | 大文字のカリグラフィ体          |


- ベクトルや行列を太字のに`\mathbf`や`\bm`等を使っても良いですが，論文内で統一すること
- 分野によっては，ベクトルや行列を太字にしない場合もありますが，信号処理分野では基本的にベクトルや行列は太字にします．（深層学習の論文だと太字にしない場合が多い気がします）
- 私は集合を大文字のカリグラフィ体で表すことが多いです．他にカリグラフィを割り当てたいものがあれば，集合を大文字のイタリック体で表す場合もあります．

--- 

| 対象               | LaTeXでの表記 | 表示例                                 | 基本的な規則・使用例           |
| ------------------------------| ------------ | ------------------ | -------------------- |
| 演算記号        | `\log`, `\exp`, `\operatorname{rank}`| $\log,\ \exp,\ \operatorname{rank}$ | 立体で表記する              |
| 数学定数       | `\mathrm{e}`, `\mathrm{i}`  | $\mathrm{e},\ \mathrm{i}$           | 分野や投稿先の規則に合わせる |
| 微分記号       | `\mathrm{d}x`  | $\mathrm{d}x$                       | 立体で表記することが多い    |


LaTeXの標準にはない演算記号はプリアンブルに`\DeclareMathOperator`で定義するとよいです．

```latex
\DeclareMathOperator*{\argmin}{arg\,min}
\DeclareMathOperator*{\argmax}{arg\,max}
\DeclareMathOperator{\tr}{tr}
\DeclareMathOperator{\rank}{rank}
\DeclareMathOperator{\diag}{diag}
```

- 上のように定義すれば，argmin_xを`\argmin_{\boldsymbol{x}}`のように書くことができる．
- `\DeclareMathOperator`のあとにアスタリスクをつけるのは，下付き文字を演算子の真下に配置できるようにするためです．

---

### 数空間

| 対象                  | LaTeXでの表記                               | 表示例                               |
| ------------------- | --------------------------------------- | --------------------------------- |
| 自然数全体               |  `\mathbb{N}`                    | $\mathbb{N}$                      |
| 整数全体                |  `\mathbb{Z}`                    | $\mathbb{Z}$                      |
| 有理数全体               |  `\mathbb{Q}`                    | $\mathbb{Q}$                      |
| 実数全体                | `\mathbb{R}`                     | $\mathbb{R}$                      |
| 複素数全体               | `\mathbb{C}`                | $\mathbb{C}$                      |
| 非負実数全体              | `\mathbb{R}_{\geq 0}`             | $\mathbb{R}_{\geq 0}$             |
| 正の実数全体              | `\mathbb{R}_{>0}`            | $\mathbb{R}_{>0}$                 |
| $n$ 次元実ベクトル空間       | `\mathbb{R}^n`                    | $\mathbb{R}^n$                    |
| $n$ 次元複素ベクトル空間      |  `\mathbb{C}^n`                 | $\mathbb{C}^n$                    |
| $m\times n$ 実行列の集合  |  `\mathbb{R}^{m \times n}`         | $\mathbb{R}^{m\times n}$          |
| $m\times n$ 複素行列の集合 |  `\mathbb{C}^{m \times n}`          | $\mathbb{C}^{m\times n}$          |


---

### 数式中の単語や略記は，変数の積として誤読されない立体で表しましょう

（正） $\boldsymbol{x}_{\min}$，$\boldsymbol{x}_{\mathrm{train}}$
（誤） $\boldsymbol{x}_{min}$，$\boldsymbol{x}_{train}$

### `\text`と`\mathrm`を使いわけましょう

| コマンド           | 主な用途              | 内容の扱い      | 例                               |
| -------------- | ----------------- | ---------- | ------------------------------- |
| `\text{...}`   | 数式中に自然言語の語句・説明を書く | 文章として扱う | `x>0\ \text{if } y>0`, `\text{subject to}` |
| `\mathrm{...}` | 数学記号の一部を立体にする  | 数式として扱う    | `\mathrm{d}x`, `\boldsymbol{x}_{\mathrm{train}}` |

---

# 参考文献に関するルール

参考文献のフォーマットが統一されていないと，めちゃくちゃ印象が悪くなります．参考文献を完璧に書けるようにしましょう．

## 投稿する学会・論文誌のルールに従うこと！！

- 投稿する学会・論文誌ごとに参考文献のスタイルは異なります
- 国内学会等で特に規定がない場合には，本研究室ではIEEE形式を採用します

## `BibTeX`を使いましょう！！

`BibTeX`を使うと，以下のメリットがあります:

- 著者名、論文名、雑誌名、巻、号、ページ、発行年などを、指定した参考文献スタイルに従って整形できる
- 本文中で文献を追加・削除・並べ替えても、引用番号と参考文献一覧が自動的に更新される
- IEEE、ACM、Elsevierなど、投稿先に応じて参考文献スタイルを切り替えやすい

手作業で参考文献を書くとミスや表記ゆれが発生しやすくなるので，必ず`BibTeX`を使ってください．

---

# `BibTeX`の使い方

## 1. 文献情報をまとめた`bib`ファイルを用意する

研究室のメンバーは文献管理に`Zotero`を使っていると思います．`Zotero`に登録されている論文は自動で`bib`ファイルを生成することができます．（`Better BibTeX`というアドオンが必要です）

1. 引用したい論文を選択します．（もちろん複数選択可．`bib`ファイルには本文で引用しない論文が含まれていても問題ないので，ひとまず全ての論文を選択しても良いです）
2. 右クリックをして，`Export Items ...`をクリックし，フォーマットは`Better BibTeX`を指定しすると，`bib`ファイルが生成される．

---

## (補足) `.bib`ファイルの中身

`.bib`ファイルには以下のように文献情報が保存されています．

```latex
@article{shuman2013,
  title = {The Emerging Field of Signal Processing on Graphs: {{Extending}} High-Dimensional Data Analysis to Networks and Other Irregular Domains},
  author = {Shuman, D. I. and Narang, S. K. and Frossard, P. and Ortega, A. and Vandergheynst, P.},
  year = 2013,
  journal = {IEEE Signal Process. Mag.},
  volume = {30},
  number = {3},
  pages = {83--98}
}
```

- `shuman2013`の部分が本文から文献を参照するための引用キーです．
- `@article`の部分がBibTeXのエントリ種別です．エントリ種別は以下のものがあります．
    - 学術雑誌論文：`@article`
    - 国際会議論文：`@inproceedings`
    - 書籍：`@book`
    - 書籍中の章：`@incollection`

---

## 2. `.tex`ファイル内に設定するコマンドを書く

`.tex`ファイルの本文の末尾（`\end{document}`の直前）に以下を書きます．

```latex
\bibliographystyle{IEEEtran}
\bibliography{references}
```

- `\bibliographystyle`は参考文献一覧をどのような書式で整形するかを指定します．
- `IEEEtran`の部分には学会から提供されている`.bst`ファイル名を書きます．IEEE Trans.系では，`IEEEtran.bst`というファイルが提供されています．
  
- `\bibliography`は書誌情報を格納したBibTeXデータベースを指定します
- `references`の部分には自分で用意した`.bib`ファイルのファイル名を指定します．

---

## 3. 本文中で文献を引用する

本文中では`\cite`を使って引用します．

```latex
Previous studies have addressed this problem~\cite{shuman2013}
```

- `shuman2013`の部分は`.bib`に記載されている文献情報の参照キー (citation key) です．
- 複数の文献を引用する場合，`\cite{shuman2013, dong2016}`のように記述します．
- `\cite`の前に`~`をつけることで，文献番号が文頭に来ることを防ぐことができます．

---

# BibTeXを使ってもまだ完璧ではない！

## 論文タイトルのスタイルを統一する

- 投稿先のスタイルがTitle Caseまたはsentence caseなのかを確認しましょう！
- Zoteroで管理していても，論文のタイトルはTitle Caseとsentence caseが混じってしまうので注意！
- IEEE Trans.系はsentence caseなので，きちんと統一しましょう！

### Title Case

- 冠詞や前置詞以外の単語の最初の文字を全て大文字にするフォーマット．
- (例: AI-Enhanced X-Ray Diffraction Analysis: Towards Real-Time Mineral Phase Identification and Quantification)

### Sentence Case

 - タイトルの先頭語，コロンに続く副題の先頭語，固有名詞，略語・頭文字のみを大文字にするフォーマット．
 - （例: AI-enhanced X-ray diffraction analysis: Towards real-time mineral phase identification and quantification）

---

## 論文誌名・国際会議のプロシーディングスの表記を統一する

国際会議のプロシーディングスは特に注意しましょう．
BibTeX形式で保存するときに表記ゆれしている場合が多いです．

### 表記ゆれの例 (ICASSPを引用する場合)

- `Proc. ICASSP`
- `Proc. IEEE Int. Conf. Acoust., Speech Signal Process.`
- `Proceedings IEEE International Conference on Acoustics, Speech, and Signal Processing`

上のような表記が入れ混じっていてダメです．一つに統一しましょう．どれに統一するかは，投稿する論文誌のフォーマットに従いましょう．

IEEE形式では，
- `Proc. IEEE Int. Conf. Acoust., Speech Signal Process.`

が採用されています．IEEE Trans.では論文誌も国際会議のプロシーディングスも単語を省略して表記するのが一般的です．

---

## (補足)　論文誌名を省略表記にする

### Zoteroで論文誌名を省略表記にした`.bib`ファイルを生成する

Zoteroで`Export Items ...`するときに，`Use Journal Abbreviation`を選択しておくと，論文誌名は省略表記になります．一方で，国際会議名は省略表記にならないので，自分で統一した表記に書き直しましょう．

## (補足)　国際会議のプロシーディングスを省略表記にする

- ICASSPは`Proc. IEEE Int. Conf. Acoust., Speech Signal Process.` 
- NeurIPSは`Proc. Adv. Neural Inf.Process. Syst.`
- ICMLは`Proc. Int. Conf. Mach. Learn`
- ICLRは`Proc. Int. Conf. Learn. Represent.`
- AISTATSは`Proc. Int. Conf. Artif.Intell. Statist.`
- CVPRは`Proc. IEEE Conf. Comput. Vis. Pattern Recognit.`
- ICCVは`Proc. IEEE Int. Conf. Comput.Vis.`

プロシーディングス名の略称が見つからない場合は，[List of Title Word Abbreviations](https://marcinwrochna.github.io/abbrevIso/)を使います．今は`.bib`ファイルをChatGPT等に投げて指示すれば，書き直してくれると思います．

---

## 査読済みの正式な出版が存在する場合，原則としてarXiv版ではなく正式版を引用する

- 論文誌や国際会議のプロシーディングスに載っているのにarXiv論文として引用するのはNG．
- arXiv版にのみ存在する内容を参照する場合などは，必要に応じてpreprintを引用してよいですが，そのようなケースは稀です．

## BibTeXのエントリ種別が正しいかを確認する

- Zoteroに論文情報を追加するときに，国際会議のプロシーディングスのBibTeXのエントリ種別が`@book`や`@article`になっている場合があります．その場合は`@inproceedings`に修正しましょう．

---

## 表示される参考文献のフォーマットが正しいかをチェックする

- `BibTeX`を使えば指定したスタイルに整形されますが，投稿する論文誌に掲載されている論文の参考文献欄を読んだりガイドラインを確認して，どういう形式で表示されるのかを理解しておいてください．
- 自分でチェックしたときに，ミスを検知しやすくなります．

### IEEE形式の場合

#### 論文誌

D. Thanou, D. I Shuman, and P. Frossard, "Learning parametric dictionaries for signals on graphs," *IEEE Trans. Signal Process.*, vol. 62, no. 15, pp. 3849–3862, Aug. 2014.

`著者名，論文タイトル，論文誌名，巻，号, ページ番号, 出版月，出版年`の順で表示されます．

#### 国際会議のプロシーディングス

X. Zhang, X. Dong, and P. Frossard, "Learning of structured graph dictionaries," in *Proc. IEEE Int. Conf. Acoust., Speech Signal Process.*, 2012, pp. 3373–3376.

`著者名，論文タイトル，プロシーディングス名，発表年，ページ番号`の順で表示されます．プロシーディングス名の前に`in`がつくことにも注意！

---

# アカデミックライティングの基礎を学ぶ

---

# ライティングでは何が重要か？


## 「文を正しく書く技術」と「論理構成・ストーリー構成」の2本柱

### 文を正しく書くとは？

- 文法的に成立している
- 一義的に読める
- 不必要に長い文章を使わず，簡潔に表現している
- 技術的に正確である

初めて論文を書く学生はこれらのことができていない場合が多いです．
文を正しく書くためには，まずはどのような文章を書くべきかを学びましょう．

### 論理構成・ストーリー構成

論文をどのように構成するかも非常に重要です．
文が正しく書けていても論理構成が無茶苦茶だと，全て書き直しになってしまいます．
どのように論理構成をすべきか，どういった内容を含める必要があるのかを学びましょう．

---

# 文を正しく書く技術：日本語編

## 書籍を読みましょう

文を正しく書くのに必要なテクニックは多くの書籍で紹介されています．なので，文を正しく書く技術はこのスライドでは詳しく解説しません．これから挙げる本は研究室に1冊はおいてありますが，文章のスキルは卒業後も役立つことが多いので，自分で購入しておくと良いです．

### [結城浩，数学文章作法 基本編，ちくま学芸文庫](https://www.chikumashobo.co.jp/product/9784480095251/)

**初めて論文を書く人は，まずこの本を必ず読んでください**．この本では，数式についてだけ書かれているわけではなく，あらゆる種類の文章に共通する心がけも書かれています．[推敲編の本](https://www.chikumashobo.co.jp/product/9784480095268/)もあって，こちらもおすすめです．

### [阿部紘久，文章力の基本，日本実業出版社](https://www.njg.co.jp/book/9784534045881/)

文章を書く基本が抑えられていない人は，この本も読むと良いです．わかりやすい文章を書くための基本ルールが例題とともにまとまっていておすすめです．

上記の2冊を読み込んで，文を正しく書く技術の基本を習得しましょう．文章執筆において[理科系の作文技術](https://www.chuko.co.jp/shinsho/1981/09/100624.html)や[日本語の作文技術](https://publications.asahi.com/product/17593.html)は名著とされているので，興味がある人は読んでみても良いと思います．ですが，山田はそこまでおすすめしないです（これらの本は初心者向けではなく，初心者の教材としては内容が冗長だと感じます）．

---

# 文を正しく書く技術：英語編

## 書籍を読みましょう

今は生成AIで文法的に正しい英語を書くことは容易になりました．しかし，どういった英文が明快なのか，どういった表現が好ましいのかを理解しておいた方が，生成AIを使った英文の推敲・添削もしやすくなります．

### [中山裕木子，英語論文ライティング教本 ―正確・明確・簡潔に書く技法，講談社](https://www.kodansha.co.jp/book/products/0000149106)

英語論文を初めて書く人は，**まずはこの本を読んでください**．この本を読めば，どのような英文を書くべきかを理解できると思います．3C (Correct, Clear Concise) を満たす英語の書き方の基礎が身につきます．

### [Adrian Wallwork，ネイティブが教える日本人研究者のための論文の書き方・アクセプト術，講談社](https://www.kspub.co.jp/book/detail/5120446.html)

この本もおすすめです．文を正しく書く技術に関しては，この本の「第1部 英語ライティングのテクニック」に役立つ情報がまとまっています．分厚い本ですし，上の本と内容が重複する部分も多いので，辞書的に使うのが良いかと思います．

---

# 論理構成・ストーリー構成

論文の構成については，良記事がいくつかあります．これらの記事は必ず読んでおいてください．

### [伝わる論文を書くための心得 ～AI系トップ会議突破の執筆術～](https://note.com/taniai_phd/m/m2721f682739d)

論文の主な構成である，Introduction, Related Work, Problem & Method, Experiments, Discussion, Conclusionsに関して，どう書くべきか・何を書くべきかが詳しく解説されています．

### [研究論文の書き方 - How to write a scientific paper](https://www.slideshare.net/slideshow/how-to-write-a-scientific-paper-48c5/276637404)

CyberAgent AI Labの研究論文の書き方に関する研修資料です．Computer Vision分野の有名論文を例に挙げながら，論文をどう書くかを解説しています．

### [機械学習、NLP論文の書き方（英語）](https://zenn.dev/kotoba_tech/articles/e4f0b6203fe869)

自然言語処理 (NLP) の論文を例に挙げながら，論文を書く際のコツを解説しています．

---

## 論理構成・ストーリー構成で参考になる書籍

### [Varanya Chaubey, 迷走しない！英語論文の書き方 秘密は「構造」作りにあり，講談社](https://www.kspub.co.jp/book/detail/5259795.html)

論文の「構造」にフォーカスした本です．経済系の論文を例に挙げながら，論文の主張点を明確にする方法や，アウトラインの構築方法，パラグラフの執筆方法が記載されています（他分野の人でも役に立ちますが，注意が必要な部分もあります）．後述する「研究室の論文執筆の流れ」はこの本をベースにしています．

### [Adrian Wallwork，ネイティブが教える日本人研究者のための論文の書き方・アクセプト術，講談社](https://www.kspub.co.jp/book/detail/5120446.html)

第2部 論文構成のテクニックのところに，IntroductionやMethodsなどの章で何を書くべきかが解説されています．
辞書的に使うのが便利かと思います．

---

# 研究室の論文執筆の流れ

---

# 論文執筆を始める前に準備をしよう

初めて論文を書く人に，「じゃあ論文書いて初稿出して」というのは少しハードルが高いかと思います．
なので，まずは以下の資料を作成して，教員と論文の内容について認識合わせをしましょう．そうすることで，手戻りも少なくなりますし，まず何に手をつけていいかが明確になります．

### 1. RAPに関する資料

これから書く論文の「R: Rsearch question / Research objective」，「A: Answer」，「P: Positioning statement」を記載した資料です．これが論文のコアロジックになります．

### 2. Claim-Evidence関する資料

論文で行う主張にEvidence (実験結果など) があるかをチェックするための資料です．

### 3. 論文のアウトラインに関する資料

アウトライン（論文の見出しなど）を書くことによって，論文に何を書くか・どう展開していくかをチェックするための資料です．また，Introductionを書くのが一番難しいので，まずはどのような論理展開をするのかを簡単にまとめるために，Introductionの骨子も書きます．


---

# 論理構成の基本: RAPとは？

RAPは，[Varanya Chaubey，迷走しない！英語論文の書き方 秘密は「構造」作りにあり，講談社](https://www.kspub.co.jp/book/detail/5259795.html)で解説されている，論文全体を支える中核的な論理のことです．R・A・Pをそれぞれ短い文章で表し，これらの論理的な組み合わせによって「この論文にはどのような貢献があるのか」に答えます．

### R: Rsearch question / Research objective

論文で解決する技術課題，または達成する研究目標を記述する

### A: Answer

Rで示した課題を，どういった原理・着想で解決するか？また，その方法により，どのような結果が得られたかを記述する．

### P: Positioning statement

「すでに知られていること / できていること」と「知ることができたら（あるいは実現したら）有益なこと」を
明確に分けて示すことで，学問分野におけるRとAの位置付けを，読み手が理解できるように記述する．

### 説明の簡便性のため，P → R → Aの順番に詳しく説明します．

---

# P: Positioning statement

## 既存研究で既に達成されていること、まだ達成されていない課題を明らかにする

自身の研究をこれまでの既存研究の文脈の中で，どう位置付けるかを明確にします．以下の項目は少なくとも明らかにする必要があります．

1. 既存研究によって何が達成されているか？
2. これまでの研究群では，どの条件・用途・評価軸で，何が不足しているか？
3. その不足を解消することが、なぜ対象読者にとって重要か？

研究の位置付けを明確化するのは，論文執筆の中でも最も難しい作業の一つです．まず，前提として自身が取り組んでいる研究の領域の概観を理解するために，たくさんの既存研究の論文を読む必要があります．そして，その既存手法を何らかの切り口で系統づけ，自身の研究を位置付けるという抽象度の高い作業が必要になります．

このPositioning statementを明確にする作業において，先ほど紹介した連載記事の[【連載 伝わる論文】Related Workの書き方](https://note.com/taniai_phd/n/nd070fad03fcd?magazine_key=m2721f682739d)が参考になると思います．



---

# （補足）研究の位置付けにどのくらい既存研究を引用すべきか？

[【連載 伝わる論文】Related Workの書き方](https://note.com/taniai_phd/n/nd070fad03fcd?magazine_key=m2721f682739d)より引用

> Introductionではメイン文脈の一部をなぞる形で論理展開を１本の線としてまっすぐ行い、研究背景やフォーカス、問題提起などを述べます。これを踏まえ、Related Workでは、この直系の文脈Aをさらに詳しく（省略した点線の派生研究なども含めて）説明しつつ、さらに文脈Aと並行する他の文脈B・Cについても議論を加えます。

### 6ページ以下（国内学会やICASSP等のページ数が少ない国際学会）の場合

基本的には，Related Workの章を設けるほどページ数に余裕がないため，Introductionで自分の研究に最も合致する直系の文脈Aの文献群を引用するのが良いでしょう．

### Full paperの場合

上の記事で書かれているように，既存研究を整理し，文脈Aと並行する他の文脈B・Cについてそれぞれの文献群を引用して，Related Workの章で議論しましょう．

---

## 研究の位置付けの例

グラフ信号処理分野だと以下の論文が例としてわかりやすいです．

[S. Bagheri+, Spectral Graph Learning With Core Eigenvectors Prior via Iterative GLASSO and Projection, IEEE Trans. Singnal Processing, 2024](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10643489)

Introductionでは，第二段落の`Focusing on statistical approaches...`の部分で，この論文に最も合致する文脈である，`statistical approaches`に言及しています．一方で，Related Workの章では，`A. Statistical Graph Learning`，`B. Feature Graph Learning`，`C. Graph Learning in Deep Neural Networks`と文脈化して，議論をしています．

---

# R: Rsearch question / Research objective


[Varanya Chaubey，迷走しない！英語論文の書き方 秘密は「構造」作りにあり，講談社](https://www.kspub.co.jp/book/detail/5259795.html)では，RはRsearch questionとしていますが，情報系では，Rsearch questionと限定せず，Research objectiveとしても良いと思っています．Rには，次のいずれか，またはその組合せを記述すると良いでしょう．

- 解くべき技術的問題
- 設計すべき方法・システムが満たす要求
- 明らかにすべき理論的条件
- 比較・説明すべき現象
- 検証すべき中心仮説

## Rを提示するコツ

- 読者に意味が伝わりやすい明確な表現を見つけること
- 広い意味を持つ言葉でRを表現してしまうと，読者の期待と現実が離れてしまう
- 逆に表現を狭くしすぎると，読者が理解しづらくなったり，研究の貢献を限定的なものにしてしまう
- Rを過不足なく表現することが重要

---

# A: Answer

## 研究課題の解決の原理・方法，それによって成立した主張

Rで提示した研究課題を解決するための原理・方法をまとめ，論文の最も重要な主張を示しましょう．
Aには，次のいずれか，またはその組合せを記述すると良いでしょう．

- 理論保証
- 達成した性能
- 従来手法に対する優位性
- 成立条件・適用範囲
- 計算量
- 実験から得られた主要な知見


---

# RAPをうまく書けない場合

以下の原因が考えられます

### サーベイ不足

自分が対象としている研究に対して解像度が足りず，研究の位置付けができていないのかもしれません．サーベイをして研究分野に対しての解像度を上げましょう．以下はサーベイに関する参考資料です．

- [研究分野をサーベイする](https://www.slideshare.net/slideshow/itolab-how-to-survey-2017/76678583)
- [論文読みの日課について](https://joisino.hatenablog.com/entry/2023/04/10/170519)

### 実験不足

実験が足りないと，主張することに大きく制限がかかります．頑張って実験を追加し，どんなことを主張できるかを模索していきましょう．

### そもそも研究の筋が悪い

こんなことを言うのは元も子もないですが，RAPを書けない研究は筋が悪い可能性があります．潔く撤退するか，新しい軸を見つけることに注力した方が良いかもしれません．

---

# Claim-Evidenceについて

- **Claim**：論文で主張すること
- **Evidence**：その主張を支える証拠

主張の根拠が揃っているかを管理するための簡潔な設計表です．主張に対してEvidenceがないことや根拠が弱いことに気づくことができます．主張したいものについてEvidenceがない場合は，実験を追加しましょう．また，主張と根拠を結びつけることで，どのような図を作れば良いかも整理されます．

---

# 論文のアウトラインについて

## 論文の見出しとテイクアウェイを書きましょう

RAPで特定したコアロジックをわかりやすく伝えるために，論文をセクションとサブセクションに切り分けましょう．そして，各セクションに対してテイクアウェイを書きましょう．

### テイクアウェイとは？

[Varanya Chaubey，迷走しない！英語論文の書き方 秘密は「構造」作りにあり，講談社](https://www.kspub.co.jp/book/detail/5259795.html)のP. 70から引用:

> テイクアウェイは，当該セクションにおいて全ての読み手に持ち帰って (take away) ほしいメッセージを簡潔に表現したものである．その目的は，論文全体の主張におけるセクションの位置付けを読み手が把握でき，主張自体についてもより深く理解できるようにすることだ．したがってテイクアウェイには，セクションのメインメッセージ，つまりそのセクション内に書かれている主張点に関連する内容がすべて凝縮されている必要がある．

---

### テイクアウェイの具体例

セクションのテイクアウェイはセクションの始まりと最初のサブセクションの間に置かれます．

[S. Bagheri+, Spectral Graph Learning With Core Eigenvectors Prior via Iterative GLASSO and Projection, IEEE Trans. Singnal Processing, 2024](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10643489)

上の論文を例に挙げると，セクション`IV. PROJECTION OPERATOR`と`A. Matrix Set With Common K Core Eigenvectors`の間にある`We conducted three sets of experiments on synthetic data...`の部分がテイクアウェイです．

---

## Introductionではテイクアウェイではなく骨子を書きましょう

Introductionでは，RAPで特定したコアロジックをわかりやすく伝える必要があります．そのコアロジックを軸に肉付けしていくことで Introductionを書いていくのが良いです．Introductionを書くのは論文執筆で一番難しい作業の一つなので，まずは骨子を書いていきましょう．
Introductionで何を書くべきかは，前述した連載記事の[【連載 伝わる論文】Introductionの書き方](https://note.com/taniai_phd/n/nd070fad03fcd?magazine_key=m2721f682739d)が参考になります

### Introductionのパラグラフ構成を考える

Introductionのパラグラフ構成を考え，各パラグラフのトピックセンテンス（必要であれば，サポーティングセンテンス，コンクルーディングセンテンス）を書きましょう．書き方に関しては，[先生の「まずは論文の骨子を箇条書きで書いてみて」に対応する: 論文執筆の第一歩](https://shunk031.hatenablog.com/entry/lets-write-outline)を読むと参考になります．

#### パラグラフライティングを知らない人に参考になる記事・書籍

- [良い文章の書き方とコツ、重要スキル：「パラグラフライティング」の解説](https://qiita.com/sugulu_Ogawa_ISID/items/36e2370c1ba2ed3de607)
- [松浦年男，田村早苗，日本語パラグラフ・ライティング入門，研究社](https://www.kenkyusha.co.jp/book/b10090583.html)
- [高橋良子，野田直紀，E. H. Jego，日台智明，理系のパラグラフライティング，羊土社](https://www.yodosha.co.jp/yodobook/book/9784758108560/)


---

# まとめ

このコーディングガイドラインを守って実装を進めていけば，ある程度品質が保たれたコードを書けると思います．結構たくさんルールを書いたので，見落としてしまうかもしれませんが，特に研究を始めたてのときはルールを厳守しつつ実装を進めることを意識してみてください．


---



---

# この資料のライセンス

この資料は以下のGitHubリポジトリで，**CC BY-NC 4.0 ライセンス**の下で公開されています．

https://github.com/koki-yamada-lab/lab-coding-guideline

他の研究室運営をされている方々にも使いやすくなるようCC BY-NC 4.0ライセンスで公開しました．この資料はMarpを使って書いているので，Markdownで簡単に改変もできます．何か気づいた点があったり，改善した方が良い点があれば上記のGitHubリポジトリにIssue/Pull Requestをあげるか，下記，山田の連絡先までご連絡いただけるとありがたいです．

Twitter: [@KokiYamada6](https://x.com/KokiYamada6)
E-mail: k-yamada@go.tuat.ac.jp

