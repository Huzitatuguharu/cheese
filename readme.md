# チーズアカデミー

## プロダクトの紹介

チーズアカデミー FUKUOKA

---

## こだわった

### 子ども受けしそうなイメージ

- 筑紫 A 丸ゴシックを使った

  > 現代の感覚で味わい深い丸ゴシック体を設計しました。ふところの広い現代風なデザインではなく、ふところを絞ったデザインの丸ゴシック体です。「漢字」は幾何学的な直線処理ではなく、温かみのある丸みを帯びたラインを意識して設計しています。

- 〇っこく、四角いもの（入力フォーム、表など）は角をまるく

- イラストは[ソコスト](https://soco-st.com/)で統一

- アイコンは[icooon-mono](https://icooon-mono.com/)で統一

### 画面を拡大しても画像が荒くならないように

- 拡張子を「.svg」で統一
- 「.png」や「.jpeg」は使わない

---

## くるしい

### CSS の優先順位

よりタグに近い、より後から読み込まれたスタイルが優先される。

´!important´ 多用しないように.

> !important は最強で、!important を打ち消すには!important を使うしかなくなり、!important 地獄になりかねない

> クレジットカードのリボ払いと同じで、何気なく手を出した!important が将来を大きく狂わせることはよくある

強い順

1. !important
2. id
3. 親要素＋タイプセレクタ
4. class
5. タイプセレクタ (h2,p,div…)

https://zenn.dev/tak_dcxi/articles/f464f90a24f754b15dd9

https://zenn.dev/tak_dcxi/articles/65629b78ee3bf7f82c4a

https://zenn.dev/haniwaman/articles/bf392f397c8db7341881

### 上下中央揃え

ユーザースペニットで上下中央揃え登録した。

"flex": {
"prefix": "fleall",
"body": [
"display: flex;",
"justify-content: center;",
"align-items: center;",
"flex-direction: column;",
]
},

要素が少ないときは
下記コードを親要素に書く。
display: grid;
place-items: center;

### web フォントを使うときの注意

- 入力フォームなどには反映されない。

`input, select, textarea, button { font-size: 100%; font-family: inherit; } `

を css に記入する

### .svg に影をつける

画像の中のオブジェクトに影をつける →CSS で filter: drop-shadow()使う

> filter: drop-shadow()と、CSS の box-shadow プロパティの大きな違いは、SVG や PNG 画像を使ったときに drop-shadow なら画像の中のオブジェクトに影をつけてくれる点です。

### before,after の擬似要素

- content=""を書き忘れた
- position プロパティの設定の仕方を間違えてた。検証ツールで数値をいじっていたらなんとなく理解できた。気がする。

### ()や{}の閉じ忘れ

---

## 勉強になりました

### はにわまん

ccs の保守のしやすさ

- 予測
- 再利用
- 保守
- 拡張

> 予測できる・・・クラス名からどういった振る舞いをするかが想像できる
> 再利用できる・・・他の場所でも同じよう使いまわしできるパーツがある
> 保守できる・・・要素を追加・削除した際に他の要素に影響を及ぼさない
> 拡張できる・・・誰が携わっても同一の品質でコーディングできる

https://zenn.dev/haniwaman/articles/bf392f397c8db7341881

### 余白は 8 の倍数

1. 余白は正方形で統一　 → 　縦と横の余白を統一
2. 余白の大きさは要素の短辺以上
3. 要素と要素の関係の強さで余白を決める

https://speakerdeck.com/yuyaink/spacing

https://yuyakinoshita.com/blog/2019/02/10/design-by-multiple-of-8/

### あべひろし

シンプル、表示速度がはやい
http://abehiroshi.la.coocan.jp/
