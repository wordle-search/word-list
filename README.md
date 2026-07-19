# word-list
## 概要
[Wordle用正規表現検索](https://wordle-search.misondroid.cloud/)で利用する単語リストを管理しています。
単語リストとWikipediaのタイトルから「Wordleの回答になりえる」以下の条件の単語を抽出しました。
- アルファベット５文字
- 過去の回答で使用されていない

現状は２つの単語リストと過去問の合成だけですが追加の単語リストとの合成作業を公開できれば、と思っております。


## 参考にしたデータ
### [english-words](https://github.com/dwyl/english-words)
  - 習得語数: 370,100語(うち5文字のもの 15,918語)
  - もともとこれで乗り切れるんじゃないか、って思ってました。
### [英語版Wikipediaのタイトルデータ](https://dumps.wikimedia.org/enwiki/latest/)
  - 収録件数: 339,052件(アルファベット5文字のものに限定)
  - 小文字でノーマライズして重複排除

### 収録データ
- [combined.json](./combined.json): `english-words`とWikipediaのタイトルデータを合成した単語リスト
- [answers.json](./answers.json): Wordle過去問(2026/7/18分以降は自動更新)
  - 毎日15:00JSTに自動更新しています
- [words.json](./words.json): 2026/6/22現在の単語リスト