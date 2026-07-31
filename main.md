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

- 体裁・フォーマットに関してルールが多い．また，ルールの他に，暗黙的にこういうことはNGというものも多い
- 研究をわかりやすく伝えるのがそもそも難しい
- 論理構成・ストーリーを考えるのに，研究に関して深い理解が必要

## 最低限必要な知識を身につけてから論文執筆をしましょう

### 体裁・フォーマットに関するルール

このルールが遵守されていないと，読者は論文の内容の真偽に疑念を持ちます．
まずは，このルールを把握し，ルールを遵守することが重要です．


### アカデミックライティングの基礎

アカデミックライティングを学ぶことで，論文の論理構成に関するの型を知ることができます，この型を知れば，論文執筆の手がかりになります．

---

# 想定する聴衆

## まだ論文執筆に慣れていない情報系の学生がメインターゲット

- 論文執筆は分野によってフォーマットも異なりますし，好まれる論理構成の型も結構違いがあります．
- 今回は，情報系がメインターゲットですが，同じ情報系の中でも，信号処理分野，機械学習分野，Computer Vision分野などでも微妙に違いがあるので注意しましょう．
- この資料や参考文献に書いてある内容を鵜呑みにしすぎないようにしましょう．内容に違和感があったら，自身が取り組んでいる研究がよく載っている論文誌ではどうなっているかを確認しましょう．

---

# 目次

## [論文の体裁・フォーマットに関するルール](#論文の体裁・フォーマットに関するルール)

- チェックリスト，LaTeX・数式・参考文献のルール

## [コードレビュー](#コードレビューについて)

- Copilotによるコードレビュー
- 教員によるコードレビュー

## [論文執筆の流れ](#ディレクトリ構造を整理する)


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
- IEEE系はsentence caseなので，きちんと統一しましょう！

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

Zoteroで`Export Items ...`するときに，`Use Journal Abbreviation`を選択しておくと，論文誌名は省略表記になる．一方で，国際会議名は省略表記にならないので，自分で統一した表記に書き直しましょう．

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

## 査読済みの正式出版版が存在する場合，原則としてarXiv版ではなく正式版を引用する

- 論文誌や国際会議のプロシーディングスに載っているのにarXiv論文として引用するのはNG．
- arXiv版にのみ存在する内容を参照する場合などは，必要に応じてpreprintを引用してよいですが，そのようなケースは稀です．

## BibTeXのエントリ種別が正しいかを確認する

- Zoteroに論文情報を追加するときに，国際会議のプロシーディングスのBibTeXのエントリ種別が`@book`や`@article`になっている場合があります．その場合は`@inproceedings`に修正しましょう．

---

# 表示される参考文献のフォーマットが正しいかをチェックする

- `BibTeX`を使えば指定したスタイルに整形されますが，投稿する論文誌に掲載されている論文の参考文献欄を読んだりガイドラインを確認して，どういう形式で表示されるのかを理解しておいてください．
- 自分でチェックしたときに，ミスを検知しやすくなります．

### IEEE形式の場合

#### 論文誌

D. Thanou, D. I Shuman, and P. Frossard, "Learning parametric dictionaries for signals on graphs," IEEE Trans. Signal Process., vol. 62, no. 15, pp. 3849–3862, Aug. 2014.

`著者名，論文タイトル，論文誌名，vol，no, ページ番号, 出版月，出版年`の順で表示されます．

#### 国際会議のプロシーディングス

X. Zhang, X. Dong, and P. Frossard, "Learning of structured graph dictionaries," in Proc. IEEE Int. Conf. Acoust., Speech Signal Process., 2012, pp. 3373–3376.

`著者名，論文タイトル，プロシーディングス名，発表年，ページ番号`の順で表示されます．プロシーディングス名の前に`in`がつくことにも注意！

---

# まとめ

このコーディングガイドラインを守って実装を進めていけば，ある程度品質が保たれたコードを書けると思います．結構たくさんルールを書いたので，見落としてしまうかもしれませんが，特に研究を始めたてのときはルールを厳守しつつ実装を進めることを意識してみてください．

---

# この資料のライセンス

この資料は以下のGitHubリポジトリで，**CC BY-NC 4.0 ライセンス**の下で公開されています．

https://github.com/koki-yamada-lab/lab-coding-guideline

他の研究室運営をされている方々にも使いやすくなるようCC BY-NC 4.0ライセンスで公開しました．この資料はMarpを使って書いているので，Markdownで簡単に改変もできます．何か気づいた点があったり，改善した方が良い点があれば上記のGitHubリポジトリにIssue/Pull Requestをあげるか，下記，山田の連絡先までご連絡いただけるとありがたいです．

Twitter: [@KokiYamada6](https://x.com/KokiYamada6)
E-mail: k-yamada@go.tuat.ac.jp

