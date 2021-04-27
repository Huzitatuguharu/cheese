# チーズアカデミー

## プロダクトの紹介

- チーズアカデミー fukuoka

## 工夫した点，こだわった点

- 子供向けのサイトにした
- SB のサイトを参考に作った

## 苦戦した点，共有したいハマりポイントなど

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

### adobe アカウントを有効活用

- webfont を使う
- カラーパレット

https://color.adobe.com/ja/create/color-wheel

[マークダウン記法](https://qiita.com/tbpgr/items/989c6badefff69377da7#github-flavored-markdowngfm)
