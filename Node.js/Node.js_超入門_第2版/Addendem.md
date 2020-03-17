# Addendem
Javascriptが分からない人向けの付録
## スクリプト書く時の注意点
#### 文は半角が基本
#### 大文字と小文字は別の文字扱い
#### スペースは無視される
#### インデントはつけたほうがいい
#### 分の改行またはセミコロンで終わる
#### 余計なことはコメント文で
```
// コメント
/* コメ
　 ント */
```
## JavaScriptの書き方
```
<script>
...スクリプト...
</script>
```
`<h1><script>...スクリプト...</script></h1>`

## 別ファイルの操作
### <script>タグとsrc属性
`<script src="{スクリプトfilename}"></script>`
srcという属性に、読み込むスクリプトの名前を書くだけで実行される

## たくさんの分岐を作るには「Switch」
```
switch( 条件 ){
case 値1:
  ...処理...
  break;
case 値2:
  ...処理...
  break;
default;
  ...それ以外の処理...
}
```
### ifとは違う
ifは真偽の値を条件にしますが、caseは文字やテキストで「同じ値を見つける」処理をします

### 使用例
```
var month = 4;
var season;
switch(month){
  case 1: season = '冬'; break;
  case 2: season = '冬'; break;
  case 3: season = '春'; break;
  case 4: season = '春'; break;
  case 5: season = '春'; break;
  case 6: season = '夏'; break;
  case 7: season = '夏'; break;
  case 8: season = '夏'; break;
  case 9: season = '秋'; break;
  case 10: season = '秋'; break;
  case 11: season = '秋'; break;
  case 12: season = '冬'; break;
  default: season = '???';
}
document.write('<p>' + month + ’月は、' + season + 'です。');
```

## インクリメント演算子
### 変数の値を１増やしたり、減らす
`num++;`

## 「関数」について
### 書き方（１）
```
function 関数名 ( 引数 ) {
  ...処理...
```

### 書き方（２）
```
var 変数 = function 関数名 ( 引数 ) {
  ...処理...

変数() //実行
```

## 連想配列 == オブジェクト
`var obj = new Object;`
`{ キー1 : 値1, キー2 : 値2, ... }`
### プロパティとメソッド
#### プロパティ
値を他しているもののこと
#### メソッド
処理を保管しているもののこと

## コンストラクタ関数
シンプルにオブジェクトを作ることができる
### 基本系
```
function 関数名 ( 引数 ){
  this.プロパティ = 値;
  this.メソッド= function(){ ... }
}

### 使い方
`var 変数 = new コンストラクタ関数( 引数 );`
